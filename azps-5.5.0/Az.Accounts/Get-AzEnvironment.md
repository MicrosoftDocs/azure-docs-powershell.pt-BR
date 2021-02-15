---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114338"
---
# <span data-ttu-id="7e313-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e313-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="7e313-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e313-102">SYNOPSIS</span></span>
<span data-ttu-id="7e313-103">Obter pontos de extremidade e metadados para uma instância de serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e313-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="7e313-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e313-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e313-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e313-105">DESCRIPTION</span></span>
<span data-ttu-id="7e313-106">O Get-AzEnvironment cmdlet obtém pontos de extremidade e metadados para uma instância dos serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e313-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="7e313-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7e313-107">EXAMPLES</span></span>

### <span data-ttu-id="7e313-108">Exemplo 1: Obter o ambiente do AzureCloud</span><span class="sxs-lookup"><span data-stu-id="7e313-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="7e313-109">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente do AzureCloud (padrão).</span><span class="sxs-lookup"><span data-stu-id="7e313-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="7e313-110">Exemplo 2: Obter o ambiente do AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="7e313-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="7e313-111">Este exemplo mostra como obter os pontos de extremidade e os metadados para o ambiente do AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7e313-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="7e313-112">Exemplo 3: Como obter o ambiente do AzureUS Facultment</span><span class="sxs-lookup"><span data-stu-id="7e313-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="7e313-113">Este exemplo mostra como obter os pontos de extremidade e os metadados do ambiente AzureUSTabment.</span><span class="sxs-lookup"><span data-stu-id="7e313-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="7e313-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e313-114">PARAMETERS</span></span>

### <span data-ttu-id="7e313-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e313-115">-DefaultProfile</span></span>
<span data-ttu-id="7e313-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7e313-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e313-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e313-117">-Name</span></span>
<span data-ttu-id="7e313-118">Especifica o nome da instância do Azure a ser obter.</span><span class="sxs-lookup"><span data-stu-id="7e313-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="7e313-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e313-119">CommonParameters</span></span>
<span data-ttu-id="7e313-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e313-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e313-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e313-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e313-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="7e313-122">INPUTS</span></span>

### <span data-ttu-id="7e313-123">System.String</span><span class="sxs-lookup"><span data-stu-id="7e313-123">System.String</span></span>

## <span data-ttu-id="7e313-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="7e313-124">OUTPUTS</span></span>

### <span data-ttu-id="7e313-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e313-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="7e313-126">Notas</span><span class="sxs-lookup"><span data-stu-id="7e313-126">NOTES</span></span>

## <span data-ttu-id="7e313-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e313-127">RELATED LINKS</span></span>

[<span data-ttu-id="7e313-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e313-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="7e313-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e313-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="7e313-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e313-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

