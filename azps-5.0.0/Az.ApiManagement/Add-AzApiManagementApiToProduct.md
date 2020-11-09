---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281534"
---
# <span data-ttu-id="8c0c4-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="8c0c4-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="8c0c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8c0c4-103">Adiciona uma API a um produto.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-103">Adds an API to a product.</span></span>

## <span data-ttu-id="8c0c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c0c4-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c0c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c0c4-105">DESCRIPTION</span></span>
<span data-ttu-id="8c0c4-106">O cmdlet **Add-AzApiManagementApiToProduct** adiciona uma API de gerenciamento de API do Azure a um produto.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="8c0c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c0c4-107">EXAMPLES</span></span>

### <span data-ttu-id="8c0c4-108">Exemplo 1: adicionar uma API a um produto</span><span class="sxs-lookup"><span data-stu-id="8c0c4-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="8c0c4-109">Este comando adiciona a API especificada ao produto especificado.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="8c0c4-110">OS</span><span class="sxs-lookup"><span data-stu-id="8c0c4-110">PARAMETERS</span></span>

### <span data-ttu-id="8c0c4-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8c0c4-111">-ApiId</span></span>
<span data-ttu-id="8c0c4-112">Especifica a ID de uma API a ser adicionada a um produto.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="8c0c4-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="8c0c4-113">-Context</span></span>
<span data-ttu-id="8c0c4-114">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8c0c4-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8c0c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c0c4-115">-DefaultProfile</span></span>
<span data-ttu-id="8c0c4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c0c4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c0c4-117">-PassThru</span></span>
<span data-ttu-id="8c0c4-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="8c0c4-118">passthru</span></span>

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

### <span data-ttu-id="8c0c4-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8c0c4-119">-ProductId</span></span>
<span data-ttu-id="8c0c4-120">Especifica a ID do produto ao qual a API será adicionada.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="8c0c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c0c4-121">CommonParameters</span></span>
<span data-ttu-id="8c0c4-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c0c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c0c4-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c0c4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c0c4-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c0c4-124">INPUTS</span></span>

### <span data-ttu-id="8c0c4-125">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8c0c4-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8c0c4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8c0c4-126">System.String</span></span>

### <span data-ttu-id="8c0c4-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c0c4-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c0c4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c0c4-128">OUTPUTS</span></span>

### <span data-ttu-id="8c0c4-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c0c4-129">System.Boolean</span></span>

## <span data-ttu-id="8c0c4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c0c4-130">NOTES</span></span>

## <span data-ttu-id="8c0c4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c0c4-131">RELATED LINKS</span></span>

[<span data-ttu-id="8c0c4-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="8c0c4-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


