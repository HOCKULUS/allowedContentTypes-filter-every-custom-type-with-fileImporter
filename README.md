SwiftUI’s FileImporter does not show files with the .ndjson extension, even when a custom UTType is defined. Other custom extensions (e.g., .abcde) work. The reason is that .ndjson is partially recognized by Apple as a known system type, which the FileImporter internally filters out. Custom UTTypes for known but unsupported extensions are ignored.

see also https://stackoverflow.com/questions/72749915/how-can-i-have-xcodeproj-type-for-allowedcontenttypes-in-fileimporter-in-swiftui
