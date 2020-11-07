---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955839"
---
# <span data-ttu-id="14fa3-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="14fa3-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="14fa3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14fa3-102">SYNOPSIS</span></span>
<span data-ttu-id="14fa3-103">Obtém as chaves do gateway existente</span><span class="sxs-lookup"><span data-stu-id="14fa3-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="14fa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14fa3-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14fa3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14fa3-105">DESCRIPTION</span></span>
<span data-ttu-id="14fa3-106">O cmdlet **Get-AzApiManagementGatewayKey** Obtém chaves do gateway existente</span><span class="sxs-lookup"><span data-stu-id="14fa3-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="14fa3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14fa3-107">EXAMPLES</span></span>

### <span data-ttu-id="14fa3-108">Exemplo 2: obter um gateway por ID</span><span class="sxs-lookup"><span data-stu-id="14fa3-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="14fa3-109">Esse comando obtém as chaves para um gateway "0123456789".</span><span class="sxs-lookup"><span data-stu-id="14fa3-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="14fa3-110">OS</span><span class="sxs-lookup"><span data-stu-id="14fa3-110">PARAMETERS</span></span>

### <span data-ttu-id="14fa3-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="14fa3-111">-Context</span></span>
<span data-ttu-id="14fa3-112">Instância do PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="14fa3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="14fa3-113">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="14fa3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="14fa3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14fa3-114">-DefaultProfile</span></span>
<span data-ttu-id="14fa3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14fa3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14fa3-116">-Gatewayid</span><span class="sxs-lookup"><span data-stu-id="14fa3-116">-GatewayId</span></span>
<span data-ttu-id="14fa3-117">Identificador do gateway.</span><span class="sxs-lookup"><span data-stu-id="14fa3-117">Gateway identifier.</span></span>
<span data-ttu-id="14fa3-118">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="14fa3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="14fa3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14fa3-119">CommonParameters</span></span>
<span data-ttu-id="14fa3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14fa3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14fa3-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14fa3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14fa3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14fa3-122">INPUTS</span></span>

### <span data-ttu-id="14fa3-123">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="14fa3-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="14fa3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="14fa3-124">System.String</span></span>

## <span data-ttu-id="14fa3-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14fa3-125">OUTPUTS</span></span>

### <span data-ttu-id="14fa3-126">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="14fa3-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="14fa3-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14fa3-127">NOTES</span></span>

## <span data-ttu-id="14fa3-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14fa3-128">RELATED LINKS</span></span>
