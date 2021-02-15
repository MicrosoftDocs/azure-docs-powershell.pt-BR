---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118077"
---
# <span data-ttu-id="faa14-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="faa14-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="faa14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="faa14-102">SYNOPSIS</span></span>
<span data-ttu-id="faa14-103">Obtém chaves do Gateway existente</span><span class="sxs-lookup"><span data-stu-id="faa14-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="faa14-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="faa14-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faa14-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="faa14-105">DESCRIPTION</span></span>
<span data-ttu-id="faa14-106">O cmdlet **Get-AzApiManagementGatewayKey** obtém as chaves do Gateway existente</span><span class="sxs-lookup"><span data-stu-id="faa14-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="faa14-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="faa14-107">EXAMPLES</span></span>

### <span data-ttu-id="faa14-108">Exemplo 2: Obter um gateway por ID</span><span class="sxs-lookup"><span data-stu-id="faa14-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="faa14-109">Esse comando obtém as chaves de um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="faa14-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="faa14-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="faa14-110">PARAMETERS</span></span>

### <span data-ttu-id="faa14-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="faa14-111">-Context</span></span>
<span data-ttu-id="faa14-112">Instância de PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="faa14-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="faa14-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="faa14-113">This parameter is required.</span></span>

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

### <span data-ttu-id="faa14-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa14-114">-DefaultProfile</span></span>
<span data-ttu-id="faa14-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="faa14-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faa14-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="faa14-116">-GatewayId</span></span>
<span data-ttu-id="faa14-117">Identificador de gateway.</span><span class="sxs-lookup"><span data-stu-id="faa14-117">Gateway identifier.</span></span>
<span data-ttu-id="faa14-118">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="faa14-118">This parameter is required.</span></span>

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

### <span data-ttu-id="faa14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa14-119">CommonParameters</span></span>
<span data-ttu-id="faa14-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa14-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faa14-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa14-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="faa14-122">INPUTS</span></span>

### <span data-ttu-id="faa14-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="faa14-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="faa14-124">System.String</span><span class="sxs-lookup"><span data-stu-id="faa14-124">System.String</span></span>

## <span data-ttu-id="faa14-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="faa14-125">OUTPUTS</span></span>

### <span data-ttu-id="faa14-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="faa14-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="faa14-127">Notas</span><span class="sxs-lookup"><span data-stu-id="faa14-127">NOTES</span></span>

## <span data-ttu-id="faa14-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="faa14-128">RELATED LINKS</span></span>
