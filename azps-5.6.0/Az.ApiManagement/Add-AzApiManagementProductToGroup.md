---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 748dc399c68a299ef0d567fbd65ec7154061869c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885749"
---
# <span data-ttu-id="aa096-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="aa096-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="aa096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa096-102">SYNOPSIS</span></span>
<span data-ttu-id="aa096-103">Adiciona um produto a um grupo.</span><span class="sxs-lookup"><span data-stu-id="aa096-103">Adds a product to a group.</span></span>

## <span data-ttu-id="aa096-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aa096-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa096-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aa096-105">DESCRIPTION</span></span>
<span data-ttu-id="aa096-106">O cmdlet **Add-AzApiManagementProductToGroup** adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="aa096-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="aa096-107">Em outras palavras, esse cmdlet atribui um grupo a um produto.</span><span class="sxs-lookup"><span data-stu-id="aa096-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="aa096-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa096-108">EXAMPLES</span></span>

### <span data-ttu-id="aa096-109">Exemplo 1: Adicionar um produto a um grupo</span><span class="sxs-lookup"><span data-stu-id="aa096-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="aa096-110">Este comando adiciona um produto a um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="aa096-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="aa096-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aa096-111">PARAMETERS</span></span>

### <span data-ttu-id="aa096-112">-Context</span><span class="sxs-lookup"><span data-stu-id="aa096-112">-Context</span></span>
<span data-ttu-id="aa096-113">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="aa096-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="aa096-114">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="aa096-114">This parameter is required.</span></span>

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

### <span data-ttu-id="aa096-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa096-115">-DefaultProfile</span></span>
<span data-ttu-id="aa096-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="aa096-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa096-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="aa096-117">-GroupId</span></span>
<span data-ttu-id="aa096-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="aa096-118">Specifies the group ID.</span></span>
<span data-ttu-id="aa096-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="aa096-119">This parameter is required.</span></span>

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

### <span data-ttu-id="aa096-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa096-120">-PassThru</span></span>
<span data-ttu-id="aa096-121">passthru</span><span class="sxs-lookup"><span data-stu-id="aa096-121">passthru</span></span>

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

### <span data-ttu-id="aa096-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="aa096-122">-ProductId</span></span>
<span data-ttu-id="aa096-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="aa096-123">Specifies the product ID.</span></span>
<span data-ttu-id="aa096-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="aa096-124">This parameter is required.</span></span>

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

### <span data-ttu-id="aa096-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa096-125">CommonParameters</span></span>
<span data-ttu-id="aa096-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa096-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa096-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa096-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa096-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa096-128">INPUTS</span></span>

### <span data-ttu-id="aa096-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="aa096-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="aa096-130">System.String</span><span class="sxs-lookup"><span data-stu-id="aa096-130">System.String</span></span>

### <span data-ttu-id="aa096-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa096-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa096-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aa096-132">OUTPUTS</span></span>

### <span data-ttu-id="aa096-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa096-133">System.Boolean</span></span>

## <span data-ttu-id="aa096-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="aa096-134">NOTES</span></span>

## <span data-ttu-id="aa096-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa096-135">RELATED LINKS</span></span>

[<span data-ttu-id="aa096-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="aa096-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


