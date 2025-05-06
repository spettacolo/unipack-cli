# API Interna

## Classe `PackageInfo`

```python
class PackageInfo(BaseModel):
    name: str
    language: str
    installed_version: Optional[str]
    latest_version: Optional[str]
    description: Optional[str]
    repository: Optional[AnyUrl]
    documentation: Optional[AnyUrl]
    downloads: Optional[int]
