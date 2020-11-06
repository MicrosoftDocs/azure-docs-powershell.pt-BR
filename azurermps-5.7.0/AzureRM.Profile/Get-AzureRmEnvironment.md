---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ac2ac931929acee527c900071de3062c4ef5398d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432439"
---
# <span data-ttu-id="99fc2-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="99fc2-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="99fc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="99fc2-103">Obter pontos de extremidade e metadados para uma instância dos serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="99fc2-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99fc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99fc2-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99fc2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="99fc2-106">O cmdlet Get-AzureRmEnvironment Obtém pontos de extremidade e metadados para uma instância dos serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="99fc2-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="99fc2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="99fc2-108">Exemplo 1: obtendo o ambiente AzureCloud</span><span class="sxs-lookup"><span data-stu-id="99fc2-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name                                              : AzureCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.windows.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.azure.com/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=254433
ServiceManagementUrl                              : https://management.core.windows.net/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301775
ResourceManagerUrl                                : https://management.azure.com/
SqlDatabaseDnsSuffix                              : .database.windows.net
StorageEndpointSuffix                             : core.windows.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : trafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.azure.net
AzureDataLakeStoreFileSystemEndpointSuffix        : azuredatalakestore.net
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix : azuredatalakeanalytics.net
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.net
```

<span data-ttu-id="99fc2-109">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente AzureCloud (padrão).</span><span class="sxs-lookup"><span data-stu-id="99fc2-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="99fc2-110">Exemplo 2: obtendo o ambiente AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="99fc2-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="99fc2-111">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="99fc2-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="99fc2-112">Exemplo 3: obtendo o ambiente AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="99fc2-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name                                              : AzureUSGovernment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.usgovcloudapi.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.usgovcloudapi.net/
ManagementPortalUrl                               : https://manage.windowsazure.us
ServiceManagementUrl                              : https://management.core.usgovcloudapi.net/
PublishSettingsFileUrl                            : https://manage.windowsazure.us/publishsettings/index
ResourceManagerUrl                                : https://management.usgovcloudapi.net/
SqlDatabaseDnsSuffix                              : .database.usgovcloudapi.net
StorageEndpointSuffix                             : core.usgovcloudapi.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.us/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

<span data-ttu-id="99fc2-113">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="99fc2-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="99fc2-114">OS</span><span class="sxs-lookup"><span data-stu-id="99fc2-114">PARAMETERS</span></span>

### <span data-ttu-id="99fc2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99fc2-115">-DefaultProfile</span></span>
<span data-ttu-id="99fc2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99fc2-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99fc2-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="99fc2-117">-Name</span></span>
<span data-ttu-id="99fc2-118">Especifica o nome da instância do Azure a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="99fc2-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99fc2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99fc2-119">CommonParameters</span></span>
<span data-ttu-id="99fc2-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99fc2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99fc2-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99fc2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99fc2-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99fc2-122">INPUTS</span></span>

### <span data-ttu-id="99fc2-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="99fc2-123">None</span></span>
<span data-ttu-id="99fc2-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="99fc2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="99fc2-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99fc2-125">OUTPUTS</span></span>

### <span data-ttu-id="99fc2-126">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="99fc2-126">PSAzureEnvironment</span></span>

## <span data-ttu-id="99fc2-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99fc2-127">NOTES</span></span>

## <span data-ttu-id="99fc2-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99fc2-128">RELATED LINKS</span></span>

[<span data-ttu-id="99fc2-129">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="99fc2-129">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="99fc2-130">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="99fc2-130">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="99fc2-131">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="99fc2-131">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)
