# TEST
curl -X POST "http://localhost:8089/auth/realms/keycloak-db-test/protocol/openid-connect/token" ^
--header "Content-Type: application/x-www-form-urlencoded" ^
--data-urlencode "grant_type=password" ^
--data-urlencode "client_id=my_client" ^
--data-urlencode "client_secret=25a6b273-d214-4a8e-b3db-9c4606a5cb5e" ^
--data-urlencode "username=admin" ^
--data-urlencode "password=1" l jq

curl -X GET "http://localhost:8000/test/authenticated" ^
--header "Authorization: bearer eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJYVnZDdUR3dnpTM19ydlBlOHBUaTZPR2dTN2VxLTFrNnZ2WU1lRlA2VzUwIn0.eyJleHAiOjE2NzIwMzE3NjgsImlhdCI6MTY3MjAyODE2OCwianRpIjoiNTU0NjI1OWQtZTg4Yi00NWU0LWJjZTYtNWE4YTI0NWU3NGMwIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDg5L2F1dGgvcmVhbG1zL2tleWNsb2FrLWRiLXRlc3QiLCJhdWQiOlsicmVhbG0tbWFuYWdlbWVudCIsIk15LWFwcDEiLCJhY2NvdW50Il0sInN1YiI6IjYxOTFkOGRjLWYxOGMtNDZiMC1hOGY3LTEwZGRkOWJiNGFhMCIsInR5cCI6IkJlYXJlciIsImF6cCI6Im15X2NsaWVudCIsInNlc3Npb25fc3RhdGUiOiIxNzA4ZmQ2ZC1jZjUxLTQzZGQtOTY5Yy1jNjk1M2U3NTE0NTkiLCJhY3IiOiIxIiwiYWxsb3dlZC1vcmlnaW5zIjpbImh0dHA6Ly9sb2NhbGhvc3Q6ODA4MSJdLCJyZWFsbV9hY2Nlc3MiOnsicm9sZXMiOlsidXNlcjIiLCJvZmZsaW5lX2FjY2VzcyIsInVtYV9hdXRob3JpemF0aW9uIiwiZGVmYXVsdC1yb2xlcy1rZXljbG9hay1kYi10ZXN0IiwiVVNFUiIsInVzZXIiXX0sInJlc291cmNlX2FjY2VzcyI6eyJyZWFsbS1tYW5hZ2VtZW50Ijp7InJvbGVzIjpbInZpZXctaWRlbnRpdHktcHJvdmlkZXJzIiwidmlldy1yZWFsbSIsIm1hbmFnZS1pZGVudGl0eS1wcm92aWRlcnMiLCJpbXBlcnNvbmF0aW9uIiwicmVhbG0tYWRtaW4iLCJjcmVhdGUtY2xpZW50IiwibWFuYWdlLXVzZXJzIiwicXVlcnktcmVhbG1zIiwidmlldy1hdXRob3JpemF0aW9uIiwicXVlcnktY2xpZW50cyIsInF1ZXJ5LXVzZXJzIiwibWFuYWdlLWV2ZW50cyIsIm1hbmFnZS1yZWFsbSIsInZpZXctZXZlbnRzIiwidmlldy11c2VycyIsInZpZXctY2xpZW50cyIsIm1hbmFnZS1hdXRob3JpemF0aW9uIiwibWFuYWdlLWNsaWVudHMiLCJxdWVyeS1ncm91cHMiXX0sIk15LWFwcDEiOnsicm9sZXMiOlsidW1hX3Byb3RlY3Rpb24iLCJBRE1JTiIsIlVTRVIiXX0sIm15X2NsaWVudCI6eyJyb2xlcyI6WyJST0xFX1VTRVIiLCJST0xFX0FETUlOIl19LCJhY2NvdW50Ijp7InJvbGVzIjpbIm1hbmFnZS1hY2NvdW50Iiwidmlldy1hcHBsaWNhdGlvbnMiLCJ2aWV3LWNvbnNlbnQiLCJtYW5hZ2UtYWNjb3VudC1saW5rcyIsIm1hbmFnZS1jb25zZW50IiwiZGVsZXRlLWFjY291bnQiLCJ2aWV3LXByb2ZpbGUiXX19LCJzY29wZSI6ImJyb3dzZXIgcHJvZmlsZSBlbWFpbCIsImVtYWlsX3ZlcmlmaWVkIjpmYWxzZSwicHJlZmVycmVkX3VzZXJuYW1lIjoiYWRtaW4ifQ.OzGNNN1rcdk67g56okSNJ7xoV1dGb-VB-yhGiwRTDLj3NRLlLezkWP7O2E0On-ToCjd2Zt07GM-LoOJXi08hE3IcScrZnvRXXUkprR-H6xefKMlTrNJEJPeLyRmjEmWnHkuEj9jZd-yHi-B3XSF2GIoaKT1ma2WJTHDQVoiZEAbnrHtZVHaVcNkbFWoIHG-9kYu-vsiXFilzUaVB_u2BUeiJen6I7UDMOUXldfvDzPxPUcq8zUZBKZtqDqOagaoNiGXQSDq5FOqrURESU4R8DtVdVIYYZrC9RjBATmDEhu18kN-CrylNuSC4cMu-T79gnnSgovpHX2zHn08soCUMlw"

curl -X GET "http://localhost:8000/test/admin" ^
--header "Authorization: bearer eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJYVnZDdUR3dnpTM19ydlBlOHBUaTZPR2dTN2VxLTFrNnZ2WU1lRlA2VzUwIn0.eyJleHAiOjE2NzIwMzE3NjgsImlhdCI6MTY3MjAyODE2OCwianRpIjoiNTU0NjI1OWQtZTg4Yi00NWU0LWJjZTYtNWE4YTI0NWU3NGMwIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDg5L2F1dGgvcmVhbG1zL2tleWNsb2FrLWRiLXRlc3QiLCJhdWQiOlsicmVhbG0tbWFuYWdlbWVudCIsIk15LWFwcDEiLCJhY2NvdW50Il0sInN1YiI6IjYxOTFkOGRjLWYxOGMtNDZiMC1hOGY3LTEwZGRkOWJiNGFhMCIsInR5cCI6IkJlYXJlciIsImF6cCI6Im15X2NsaWVudCIsInNlc3Npb25fc3RhdGUiOiIxNzA4ZmQ2ZC1jZjUxLTQzZGQtOTY5Yy1jNjk1M2U3NTE0NTkiLCJhY3IiOiIxIiwiYWxsb3dlZC1vcmlnaW5zIjpbImh0dHA6Ly9sb2NhbGhvc3Q6ODA4MSJdLCJyZWFsbV9hY2Nlc3MiOnsicm9sZXMiOlsidXNlcjIiLCJvZmZsaW5lX2FjY2VzcyIsInVtYV9hdXRob3JpemF0aW9uIiwiZGVmYXVsdC1yb2xlcy1rZXljbG9hay1kYi10ZXN0IiwiVVNFUiIsInVzZXIiXX0sInJlc291cmNlX2FjY2VzcyI6eyJyZWFsbS1tYW5hZ2VtZW50Ijp7InJvbGVzIjpbInZpZXctaWRlbnRpdHktcHJvdmlkZXJzIiwidmlldy1yZWFsbSIsIm1hbmFnZS1pZGVudGl0eS1wcm92aWRlcnMiLCJpbXBlcnNvbmF0aW9uIiwicmVhbG0tYWRtaW4iLCJjcmVhdGUtY2xpZW50IiwibWFuYWdlLXVzZXJzIiwicXVlcnktcmVhbG1zIiwidmlldy1hdXRob3JpemF0aW9uIiwicXVlcnktY2xpZW50cyIsInF1ZXJ5LXVzZXJzIiwibWFuYWdlLWV2ZW50cyIsIm1hbmFnZS1yZWFsbSIsInZpZXctZXZlbnRzIiwidmlldy11c2VycyIsInZpZXctY2xpZW50cyIsIm1hbmFnZS1hdXRob3JpemF0aW9uIiwibWFuYWdlLWNsaWVudHMiLCJxdWVyeS1ncm91cHMiXX0sIk15LWFwcDEiOnsicm9sZXMiOlsidW1hX3Byb3RlY3Rpb24iLCJBRE1JTiIsIlVTRVIiXX0sIm15X2NsaWVudCI6eyJyb2xlcyI6WyJST0xFX1VTRVIiLCJST0xFX0FETUlOIl19LCJhY2NvdW50Ijp7InJvbGVzIjpbIm1hbmFnZS1hY2NvdW50Iiwidmlldy1hcHBsaWNhdGlvbnMiLCJ2aWV3LWNvbnNlbnQiLCJtYW5hZ2UtYWNjb3VudC1saW5rcyIsIm1hbmFnZS1jb25zZW50IiwiZGVsZXRlLWFjY291bnQiLCJ2aWV3LXByb2ZpbGUiXX19LCJzY29wZSI6ImJyb3dzZXIgcHJvZmlsZSBlbWFpbCIsImVtYWlsX3ZlcmlmaWVkIjpmYWxzZSwicHJlZmVycmVkX3VzZXJuYW1lIjoiYWRtaW4ifQ.OzGNNN1rcdk67g56okSNJ7xoV1dGb-VB-yhGiwRTDLj3NRLlLezkWP7O2E0On-ToCjd2Zt07GM-LoOJXi08hE3IcScrZnvRXXUkprR-H6xefKMlTrNJEJPeLyRmjEmWnHkuEj9jZd-yHi-B3XSF2GIoaKT1ma2WJTHDQVoiZEAbnrHtZVHaVcNkbFWoIHG-9kYu-vsiXFilzUaVB_u2BUeiJen6I7UDMOUXldfvDzPxPUcq8zUZBKZtqDqOagaoNiGXQSDq5FOqrURESU4R8DtVdVIYYZrC9RjBATmDEhu18kN-CrylNuSC4cMu-T79gnnSgovpHX2zHn08soCUMlw"

curl -X GET "http://localhost:8000/test/user" ^
--header "Authorization: bearer eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJYVnZDdUR3dnpTM19ydlBlOHBUaTZPR2dTN2VxLTFrNnZ2WU1lRlA2VzUwIn0.eyJleHAiOjE2NzIwMzE3NjgsImlhdCI6MTY3MjAyODE2OCwianRpIjoiNTU0NjI1OWQtZTg4Yi00NWU0LWJjZTYtNWE4YTI0NWU3NGMwIiwiaXNzIjoiaHR0cDovL2xvY2FsaG9zdDo4MDg5L2F1dGgvcmVhbG1zL2tleWNsb2FrLWRiLXRlc3QiLCJhdWQiOlsicmVhbG0tbWFuYWdlbWVudCIsIk15LWFwcDEiLCJhY2NvdW50Il0sInN1YiI6IjYxOTFkOGRjLWYxOGMtNDZiMC1hOGY3LTEwZGRkOWJiNGFhMCIsInR5cCI6IkJlYXJlciIsImF6cCI6Im15X2NsaWVudCIsInNlc3Npb25fc3RhdGUiOiIxNzA4ZmQ2ZC1jZjUxLTQzZGQtOTY5Yy1jNjk1M2U3NTE0NTkiLCJhY3IiOiIxIiwiYWxsb3dlZC1vcmlnaW5zIjpbImh0dHA6Ly9sb2NhbGhvc3Q6ODA4MSJdLCJyZWFsbV9hY2Nlc3MiOnsicm9sZXMiOlsidXNlcjIiLCJvZmZsaW5lX2FjY2VzcyIsInVtYV9hdXRob3JpemF0aW9uIiwiZGVmYXVsdC1yb2xlcy1rZXljbG9hay1kYi10ZXN0IiwiVVNFUiIsInVzZXIiXX0sInJlc291cmNlX2FjY2VzcyI6eyJyZWFsbS1tYW5hZ2VtZW50Ijp7InJvbGVzIjpbInZpZXctaWRlbnRpdHktcHJvdmlkZXJzIiwidmlldy1yZWFsbSIsIm1hbmFnZS1pZGVudGl0eS1wcm92aWRlcnMiLCJpbXBlcnNvbmF0aW9uIiwicmVhbG0tYWRtaW4iLCJjcmVhdGUtY2xpZW50IiwibWFuYWdlLXVzZXJzIiwicXVlcnktcmVhbG1zIiwidmlldy1hdXRob3JpemF0aW9uIiwicXVlcnktY2xpZW50cyIsInF1ZXJ5LXVzZXJzIiwibWFuYWdlLWV2ZW50cyIsIm1hbmFnZS1yZWFsbSIsInZpZXctZXZlbnRzIiwidmlldy11c2VycyIsInZpZXctY2xpZW50cyIsIm1hbmFnZS1hdXRob3JpemF0aW9uIiwibWFuYWdlLWNsaWVudHMiLCJxdWVyeS1ncm91cHMiXX0sIk15LWFwcDEiOnsicm9sZXMiOlsidW1hX3Byb3RlY3Rpb24iLCJBRE1JTiIsIlVTRVIiXX0sIm15X2NsaWVudCI6eyJyb2xlcyI6WyJST0xFX1VTRVIiLCJST0xFX0FETUlOIl19LCJhY2NvdW50Ijp7InJvbGVzIjpbIm1hbmFnZS1hY2NvdW50Iiwidmlldy1hcHBsaWNhdGlvbnMiLCJ2aWV3LWNvbnNlbnQiLCJtYW5hZ2UtYWNjb3VudC1saW5rcyIsIm1hbmFnZS1jb25zZW50IiwiZGVsZXRlLWFjY291bnQiLCJ2aWV3LXByb2ZpbGUiXX19LCJzY29wZSI6ImJyb3dzZXIgcHJvZmlsZSBlbWFpbCIsImVtYWlsX3ZlcmlmaWVkIjpmYWxzZSwicHJlZmVycmVkX3VzZXJuYW1lIjoiYWRtaW4ifQ.OzGNNN1rcdk67g56okSNJ7xoV1dGb-VB-yhGiwRTDLj3NRLlLezkWP7O2E0On-ToCjd2Zt07GM-LoOJXi08hE3IcScrZnvRXXUkprR-H6xefKMlTrNJEJPeLyRmjEmWnHkuEj9jZd-yHi-B3XSF2GIoaKT1ma2WJTHDQVoiZEAbnrHtZVHaVcNkbFWoIHG-9kYu-vsiXFilzUaVB_u2BUeiJen6I7UDMOUXldfvDzPxPUcq8zUZBKZtqDqOagaoNiGXQSDq5FOqrURESU4R8DtVdVIYYZrC9RjBATmDEhu18kN-CrylNuSC4cMu-T79gnnSgovpHX2zHn08soCUMlw"