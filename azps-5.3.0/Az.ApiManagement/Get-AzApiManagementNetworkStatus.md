---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: 5ba351ab1a5102acc1855e13821650b8ce1b4373
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432716"
---
# <span data-ttu-id="127c3-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="127c3-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="127c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="127c3-102">SYNOPSIS</span></span>
<span data-ttu-id="127c3-103">Obtém o status de conectividade para os recursos externos em que o serviço de gerenciamento de API depende de dentro do serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="127c3-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="127c3-104">Isso também retorna os servidores DNS como visíveis para o CloudService.</span><span class="sxs-lookup"><span data-stu-id="127c3-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="127c3-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="127c3-105">SYNTAX</span></span>

### <span data-ttu-id="127c3-106">ByInputObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="127c3-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="127c3-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="127c3-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="127c3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="127c3-108">DESCRIPTION</span></span>
<span data-ttu-id="127c3-109">Obtém o status da rede do serviço de gerenciamento de API</span><span class="sxs-lookup"><span data-stu-id="127c3-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="127c3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="127c3-110">EXAMPLES</span></span>

### <span data-ttu-id="127c3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="127c3-111">Example 1</span></span>
```powershell
PS D:\github\azure-powershell> Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice

Location DnsServers      ConnectivityStatus
-------- ----------      ------------------
West US  {168.63.129.16} {apimgmtstaoonqs7wwzjosky.blob.core.windows.net, apimgmtstaoonqs7wwzjosky.file.core.windows.net, apimgmtstaoonqs7wwzjosky.queue.core.windows.net, apimgmtstaoonqs7wwzjosk...


PS D:\github\azure-powershell> $networkStatus = Get-AzApiManagementNetworkStatus -ResourceGroupName powershelltest -Name powershellsdkservice
PS D:\github\azure-powershell> $networkStatus.ConnectivityStatus


Name             : apimgmtstaoonqs7wwzjosky.blob.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : apimgmtstaoonqs7wwzjosky.file.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.queue.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : apimgmtstaoonqs7wwzjosky.table.core.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : bx9gltecfv.database.windows.net
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:41 PM
LastStatusChange : 1/30/2019 5:31:39 PM

Name             : https://prod3.metrics.nsatc.net:1886/RecoveryService
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:07:11 PM
LastStatusChange : 4/29/2019 1:31:30 PM

Name             : prod.warmpath.msftcloudes.com
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:06:38 PM
LastStatusChange : 1/30/2019 5:31:38 PM

Name             : Scm
Status           : success
Error            :
LastUpdated      : 5/2/2019 5:04:27 PM
LastStatusChange : 4/30/2019 11:16:20 PM
```

<span data-ttu-id="127c3-112">Obtém o status de conectividade dos diferentes recursos dos quais o serviço ApiManagement depende.</span><span class="sxs-lookup"><span data-stu-id="127c3-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="127c3-113">OS</span><span class="sxs-lookup"><span data-stu-id="127c3-113">PARAMETERS</span></span>

### <span data-ttu-id="127c3-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="127c3-114">-ApiManagementObject</span></span>
<span data-ttu-id="127c3-115">Instância do PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="127c3-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="127c3-116">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="127c3-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="127c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127c3-117">-DefaultProfile</span></span>
<span data-ttu-id="127c3-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="127c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="127c3-119">-Local</span><span class="sxs-lookup"><span data-stu-id="127c3-119">-Location</span></span>
<span data-ttu-id="127c3-120">Localização do serviço de gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="127c3-120">Location of the API Management Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="127c3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="127c3-121">-Name</span></span>
<span data-ttu-id="127c3-122">Nome do gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="127c3-122">Name of API Management.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="127c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="127c3-124">Nome do grupo de recursos sob o qual existe gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="127c3-124">Name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="127c3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127c3-125">CommonParameters</span></span>
<span data-ttu-id="127c3-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127c3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127c3-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="127c3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127c3-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="127c3-128">INPUTS</span></span>

### <span data-ttu-id="127c3-129">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="127c3-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="127c3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="127c3-130">System.String</span></span>

## <span data-ttu-id="127c3-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="127c3-131">OUTPUTS</span></span>

### <span data-ttu-id="127c3-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="127c3-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="127c3-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="127c3-133">NOTES</span></span>

## <span data-ttu-id="127c3-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="127c3-134">RELATED LINKS</span></span>
