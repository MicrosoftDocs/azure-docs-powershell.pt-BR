---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116295"
---
# <span data-ttu-id="803da-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="803da-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="803da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="803da-102">SYNOPSIS</span></span>
<span data-ttu-id="803da-103">Obter pontos de extremidade e metadados para uma instância dos serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="803da-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="803da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="803da-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="803da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="803da-105">DESCRIPTION</span></span>
<span data-ttu-id="803da-106">O cmdlet Get-AzEnvironment Obtém pontos de extremidade e metadados para uma instância dos serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="803da-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="803da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="803da-107">EXAMPLES</span></span>

### <span data-ttu-id="803da-108">Exemplo 1: obtendo o ambiente AzureCloud</span><span class="sxs-lookup"><span data-stu-id="803da-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="803da-109">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente AzureCloud (padrão).</span><span class="sxs-lookup"><span data-stu-id="803da-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="803da-110">Exemplo 2: obtendo o ambiente AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="803da-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="803da-111">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="803da-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="803da-112">Exemplo 3: obtendo o ambiente AzureUSGovernment</span><span class="sxs-lookup"><span data-stu-id="803da-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="803da-113">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente AzureUSGovernment.</span><span class="sxs-lookup"><span data-stu-id="803da-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="803da-114">OS</span><span class="sxs-lookup"><span data-stu-id="803da-114">PARAMETERS</span></span>

### <span data-ttu-id="803da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="803da-115">-DefaultProfile</span></span>
<span data-ttu-id="803da-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="803da-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="803da-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="803da-117">-Name</span></span>
<span data-ttu-id="803da-118">Especifica o nome da instância do Azure a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="803da-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="803da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="803da-119">CommonParameters</span></span>
<span data-ttu-id="803da-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="803da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="803da-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="803da-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="803da-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="803da-122">INPUTS</span></span>

### <span data-ttu-id="803da-123">System. String</span><span class="sxs-lookup"><span data-stu-id="803da-123">System.String</span></span>

## <span data-ttu-id="803da-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="803da-124">OUTPUTS</span></span>

### <span data-ttu-id="803da-125">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="803da-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="803da-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="803da-126">NOTES</span></span>

## <span data-ttu-id="803da-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="803da-127">RELATED LINKS</span></span>

[<span data-ttu-id="803da-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="803da-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="803da-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="803da-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="803da-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="803da-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

