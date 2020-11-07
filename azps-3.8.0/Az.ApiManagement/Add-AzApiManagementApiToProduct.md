---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943948"
---
# <span data-ttu-id="df003-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="df003-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="df003-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df003-102">SYNOPSIS</span></span>
<span data-ttu-id="df003-103">Adiciona uma API a um produto.</span><span class="sxs-lookup"><span data-stu-id="df003-103">Adds an API to a product.</span></span>

## <span data-ttu-id="df003-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df003-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df003-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df003-105">DESCRIPTION</span></span>
<span data-ttu-id="df003-106">O cmdlet **Add-AzApiManagementApiToProduct** adiciona uma API de gerenciamento de API do Azure a um produto.</span><span class="sxs-lookup"><span data-stu-id="df003-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="df003-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df003-107">EXAMPLES</span></span>

### <span data-ttu-id="df003-108">Exemplo 1: adicionar uma API a um produto</span><span class="sxs-lookup"><span data-stu-id="df003-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="df003-109">Este comando adiciona a API especificada ao produto especificado.</span><span class="sxs-lookup"><span data-stu-id="df003-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="df003-110">OS</span><span class="sxs-lookup"><span data-stu-id="df003-110">PARAMETERS</span></span>

### <span data-ttu-id="df003-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="df003-111">-ApiId</span></span>
<span data-ttu-id="df003-112">Especifica a ID de uma API a ser adicionada a um produto.</span><span class="sxs-lookup"><span data-stu-id="df003-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="df003-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="df003-113">-Context</span></span>
<span data-ttu-id="df003-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="df003-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df003-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df003-115">-DefaultProfile</span></span>
<span data-ttu-id="df003-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df003-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df003-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df003-117">-PassThru</span></span>
<span data-ttu-id="df003-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="df003-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df003-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="df003-119">-ProductId</span></span>
<span data-ttu-id="df003-120">Especifica a ID do produto ao qual a API será adicionada.</span><span class="sxs-lookup"><span data-stu-id="df003-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="df003-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df003-121">CommonParameters</span></span>
<span data-ttu-id="df003-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df003-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df003-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df003-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df003-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df003-124">INPUTS</span></span>

### <span data-ttu-id="df003-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="df003-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="df003-126">System. String</span><span class="sxs-lookup"><span data-stu-id="df003-126">System.String</span></span>

### <span data-ttu-id="df003-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df003-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df003-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df003-128">OUTPUTS</span></span>

### <span data-ttu-id="df003-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df003-129">System.Boolean</span></span>

## <span data-ttu-id="df003-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df003-130">NOTES</span></span>

## <span data-ttu-id="df003-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df003-131">RELATED LINKS</span></span>

[<span data-ttu-id="df003-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="df003-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


