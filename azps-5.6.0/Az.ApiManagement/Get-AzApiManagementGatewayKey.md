---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: 08931af2c5d4f4747bd02a759e374d8fccd247c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889051"
---
# <span data-ttu-id="7ae2d-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="7ae2d-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="7ae2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae2d-103">Obtém chaves do Gateway existente</span><span class="sxs-lookup"><span data-stu-id="7ae2d-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="7ae2d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ae2d-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae2d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ae2d-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae2d-106">O cmdlet **Get-AzApiManagementGatewayKey** obtém chaves do Gateway existente</span><span class="sxs-lookup"><span data-stu-id="7ae2d-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="7ae2d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-107">EXAMPLES</span></span>

### <span data-ttu-id="7ae2d-108">Exemplo 2: Obter um gateway por ID</span><span class="sxs-lookup"><span data-stu-id="7ae2d-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="7ae2d-109">Este comando obtém as chaves de um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="7ae2d-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="7ae2d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-110">PARAMETERS</span></span>

### <span data-ttu-id="7ae2d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7ae2d-111">-Context</span></span>
<span data-ttu-id="7ae2d-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7ae2d-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae2d-114">-DefaultProfile</span></span>
<span data-ttu-id="7ae2d-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae2d-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7ae2d-116">-GatewayId</span></span>
<span data-ttu-id="7ae2d-117">Identificador de gateway.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-117">Gateway identifier.</span></span>
<span data-ttu-id="7ae2d-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae2d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae2d-119">CommonParameters</span></span>
<span data-ttu-id="7ae2d-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ae2d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae2d-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ae2d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae2d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-122">INPUTS</span></span>

### <span data-ttu-id="7ae2d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7ae2d-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7ae2d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7ae2d-124">System.String</span></span>

## <span data-ttu-id="7ae2d-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-125">OUTPUTS</span></span>

### <span data-ttu-id="7ae2d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="7ae2d-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="7ae2d-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ae2d-127">NOTES</span></span>

## <span data-ttu-id="7ae2d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ae2d-128">RELATED LINKS</span></span>
