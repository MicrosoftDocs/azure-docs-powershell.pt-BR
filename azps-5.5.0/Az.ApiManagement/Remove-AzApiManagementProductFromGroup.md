---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116009"
---
# <span data-ttu-id="746eb-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="746eb-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="746eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="746eb-102">SYNOPSIS</span></span>
<span data-ttu-id="746eb-103">Remove um produto de um grupo.</span><span class="sxs-lookup"><span data-stu-id="746eb-103">Removes a product from a group.</span></span>

## <span data-ttu-id="746eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="746eb-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="746eb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="746eb-105">DESCRIPTION</span></span>
<span data-ttu-id="746eb-106">O cmdlet **Remove-AzApiManagementProductFromGroup** remove um produto de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="746eb-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="746eb-107">Em outras palavras, este cmdlet remove a atribuição de grupo de um produto.</span><span class="sxs-lookup"><span data-stu-id="746eb-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="746eb-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="746eb-108">EXAMPLES</span></span>

### <span data-ttu-id="746eb-109">Exemplo 1: Remover um produto de um grupo</span><span class="sxs-lookup"><span data-stu-id="746eb-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="746eb-110">Esse comando remove um produto de um grupo existente.</span><span class="sxs-lookup"><span data-stu-id="746eb-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="746eb-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="746eb-111">PARAMETERS</span></span>

### <span data-ttu-id="746eb-112">-Contexto</span><span class="sxs-lookup"><span data-stu-id="746eb-112">-Context</span></span>
<span data-ttu-id="746eb-113">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="746eb-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="746eb-114">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="746eb-114">This parameter is required.</span></span>

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

### <span data-ttu-id="746eb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="746eb-115">-DefaultProfile</span></span>
<span data-ttu-id="746eb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="746eb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="746eb-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="746eb-117">-GroupId</span></span>
<span data-ttu-id="746eb-118">Especifica a ID do grupo.</span><span class="sxs-lookup"><span data-stu-id="746eb-118">Specifies the group ID.</span></span>
<span data-ttu-id="746eb-119">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="746eb-119">This parameter is required.</span></span>

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

### <span data-ttu-id="746eb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="746eb-120">-PassThru</span></span>
<span data-ttu-id="746eb-121">Indica que esse cmdlet retorna um valor de $True, se for bem-sucedido ou $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="746eb-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="746eb-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="746eb-122">-ProductId</span></span>
<span data-ttu-id="746eb-123">Especifica a ID do produto.</span><span class="sxs-lookup"><span data-stu-id="746eb-123">Specifies the product ID.</span></span>
<span data-ttu-id="746eb-124">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="746eb-124">This parameter is required.</span></span>

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

### <span data-ttu-id="746eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="746eb-125">CommonParameters</span></span>
<span data-ttu-id="746eb-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="746eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="746eb-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="746eb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="746eb-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="746eb-128">INPUTS</span></span>

### <span data-ttu-id="746eb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="746eb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="746eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="746eb-130">System.String</span></span>

### <span data-ttu-id="746eb-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="746eb-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="746eb-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="746eb-132">OUTPUTS</span></span>

### <span data-ttu-id="746eb-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="746eb-133">System.Boolean</span></span>

## <span data-ttu-id="746eb-134">Notas</span><span class="sxs-lookup"><span data-stu-id="746eb-134">NOTES</span></span>

## <span data-ttu-id="746eb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="746eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="746eb-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="746eb-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


