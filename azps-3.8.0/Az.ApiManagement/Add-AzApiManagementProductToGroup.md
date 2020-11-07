---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943951"
---
# <span data-ttu-id="c7f64-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="c7f64-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="c7f64-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7f64-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f64-103">Adiciona um produto a um grupo.</span><span class="sxs-lookup"><span data-stu-id="c7f64-103">Adds a product to a group.</span></span>

## <span data-ttu-id="c7f64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7f64-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f64-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7f64-105">DESCRIPTION</span></span>
<span data-ttu-id="c7f64-106">O cmdlet **Add-AzApiManagementProductToGroup** adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c7f64-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="c7f64-107">Em outras palavras, esse cmdlet atribui um grupo a um produto.</span><span class="sxs-lookup"><span data-stu-id="c7f64-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="c7f64-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7f64-108">EXAMPLES</span></span>

### <span data-ttu-id="c7f64-109">Exemplo 1: adicionar um produto a um grupo</span><span class="sxs-lookup"><span data-stu-id="c7f64-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="c7f64-110">Esse comando adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="c7f64-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="c7f64-111">OS</span><span class="sxs-lookup"><span data-stu-id="c7f64-111">PARAMETERS</span></span>

### <span data-ttu-id="c7f64-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c7f64-112">-Context</span></span>
<span data-ttu-id="c7f64-113">Especifica um objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c7f64-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="c7f64-114">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c7f64-114">This parameter is required.</span></span>

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

### <span data-ttu-id="c7f64-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f64-115">-DefaultProfile</span></span>
<span data-ttu-id="c7f64-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7f64-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7f64-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="c7f64-117">-GroupId</span></span>
<span data-ttu-id="c7f64-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="c7f64-118">Specifies the group ID.</span></span>
<span data-ttu-id="c7f64-119">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c7f64-119">This parameter is required.</span></span>

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

### <span data-ttu-id="c7f64-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7f64-120">-PassThru</span></span>
<span data-ttu-id="c7f64-121">PassThru</span><span class="sxs-lookup"><span data-stu-id="c7f64-121">passthru</span></span>

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

### <span data-ttu-id="c7f64-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c7f64-122">-ProductId</span></span>
<span data-ttu-id="c7f64-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="c7f64-123">Specifies the product ID.</span></span>
<span data-ttu-id="c7f64-124">Esse parâmetro é obrigatório.</span><span class="sxs-lookup"><span data-stu-id="c7f64-124">This parameter is required.</span></span>

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

### <span data-ttu-id="c7f64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f64-125">CommonParameters</span></span>
<span data-ttu-id="c7f64-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7f64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f64-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7f64-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f64-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7f64-128">INPUTS</span></span>

### <span data-ttu-id="c7f64-129">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7f64-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7f64-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c7f64-130">System.String</span></span>

### <span data-ttu-id="c7f64-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7f64-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7f64-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7f64-132">OUTPUTS</span></span>

### <span data-ttu-id="c7f64-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7f64-133">System.Boolean</span></span>

## <span data-ttu-id="c7f64-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7f64-134">NOTES</span></span>

## <span data-ttu-id="c7f64-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7f64-135">RELATED LINKS</span></span>

[<span data-ttu-id="c7f64-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="c7f64-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


