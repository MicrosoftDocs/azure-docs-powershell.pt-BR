---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnetworkstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNetworkStatus.md
ms.openlocfilehash: a6605b583ec821bf5eacd96270d74b084d9cafb3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889704"
---
# <span data-ttu-id="b66e1-101">Get-AzApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="b66e1-101">Get-AzApiManagementNetworkStatus</span></span>

## <span data-ttu-id="b66e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b66e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b66e1-103">Obtém o Status de Conectividade para os recursos externos nos quais o serviço de Gerenciamento de Api depende de dentro do Serviço de Nuvem.</span><span class="sxs-lookup"><span data-stu-id="b66e1-103">Gets the Connectivity Status to the external resources on which the Api Management service depends from inside the Cloud Service.</span></span> <span data-ttu-id="b66e1-104">Isso também retorna os Servidores DNS como visíveis para o CloudService.</span><span class="sxs-lookup"><span data-stu-id="b66e1-104">This also returns the DNS Servers as visible to the CloudService.</span></span>

## <span data-ttu-id="b66e1-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b66e1-105">SYNTAX</span></span>

### <span data-ttu-id="b66e1-106">ByInputObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b66e1-106">ByInputObject (Default)</span></span>
```
Get-AzApiManagementNetworkStatus -ApiManagementObject <PsApiManagement> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b66e1-107">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="b66e1-107">ExpandedParameter</span></span>
```
Get-AzApiManagementNetworkStatus -ResourceGroupName <String> -Name <String> [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b66e1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b66e1-108">DESCRIPTION</span></span>
<span data-ttu-id="b66e1-109">Obtém o status de rede de seu serviço de Gerenciamento de Api</span><span class="sxs-lookup"><span data-stu-id="b66e1-109">Gets the Network status of their Api Management service</span></span>

## <span data-ttu-id="b66e1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b66e1-110">EXAMPLES</span></span>

### <span data-ttu-id="b66e1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b66e1-111">Example 1</span></span>
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

<span data-ttu-id="b66e1-112">Obtém o status de conectividade dos diferentes recursos dos quais o serviço ApiManagement depende.</span><span class="sxs-lookup"><span data-stu-id="b66e1-112">Gets the connectivity status of the different resources on which ApiManagement service depends upon.</span></span>

## <span data-ttu-id="b66e1-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b66e1-113">PARAMETERS</span></span>

### <span data-ttu-id="b66e1-114">-ApiManagementObject</span><span class="sxs-lookup"><span data-stu-id="b66e1-114">-ApiManagementObject</span></span>
<span data-ttu-id="b66e1-115">Instância de PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b66e1-115">Instance of PsApiManagement.</span></span> <span data-ttu-id="b66e1-116">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="b66e1-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b66e1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66e1-117">-DefaultProfile</span></span>
<span data-ttu-id="b66e1-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b66e1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b66e1-119">-Location</span><span class="sxs-lookup"><span data-stu-id="b66e1-119">-Location</span></span>
<span data-ttu-id="b66e1-120">Local do Serviço de Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b66e1-120">Location of the API Management Service.</span></span>

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

### <span data-ttu-id="b66e1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b66e1-121">-Name</span></span>
<span data-ttu-id="b66e1-122">Nome do Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b66e1-122">Name of API Management.</span></span>

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

### <span data-ttu-id="b66e1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b66e1-123">-ResourceGroupName</span></span>
<span data-ttu-id="b66e1-124">Nome do grupo de recursos no qual existe o Gerenciamento de API.</span><span class="sxs-lookup"><span data-stu-id="b66e1-124">Name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="b66e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66e1-125">CommonParameters</span></span>
<span data-ttu-id="b66e1-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b66e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66e1-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b66e1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66e1-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b66e1-128">INPUTS</span></span>

### <span data-ttu-id="b66e1-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b66e1-129">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="b66e1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b66e1-130">System.String</span></span>

## <span data-ttu-id="b66e1-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b66e1-131">OUTPUTS</span></span>

### <span data-ttu-id="b66e1-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span><span class="sxs-lookup"><span data-stu-id="b66e1-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementNetworkStatus</span></span>

## <span data-ttu-id="b66e1-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="b66e1-133">NOTES</span></span>

## <span data-ttu-id="b66e1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b66e1-134">RELATED LINKS</span></span>
