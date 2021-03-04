---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888764"
---
# <span data-ttu-id="c1783-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c1783-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="c1783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1783-102">SYNOPSIS</span></span>
<span data-ttu-id="c1783-103">Remove um produto de Gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="c1783-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="c1783-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1783-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1783-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1783-105">DESCRIPTION</span></span>
<span data-ttu-id="c1783-106">O cmdlet **Remove-AzApiManagementProduct** remove um produto de Gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="c1783-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="c1783-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1783-107">EXAMPLES</span></span>

### <span data-ttu-id="c1783-108">Exemplo 1: Remover um produto existente e todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="c1783-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="c1783-109">Este comando remove um produto existente e todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="c1783-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="c1783-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1783-110">PARAMETERS</span></span>

### <span data-ttu-id="c1783-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c1783-111">-Context</span></span>
<span data-ttu-id="c1783-112">Especifica uma instância do **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="c1783-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c1783-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1783-113">-DefaultProfile</span></span>
<span data-ttu-id="c1783-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="c1783-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1783-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="c1783-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="c1783-116">Indica se é necessário excluir assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="c1783-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="c1783-117">Se você não definir esse parâmetro e as assinaturas existirem, uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="c1783-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="c1783-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1783-118">-PassThru</span></span>
<span data-ttu-id="c1783-119">Indica que esse cmdlet retornará um valor de $True, se tiver êxito, ou um valor de $False, se falhar.</span><span class="sxs-lookup"><span data-stu-id="c1783-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="c1783-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c1783-120">-ProductId</span></span>
<span data-ttu-id="c1783-121">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="c1783-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="c1783-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1783-122">-Confirm</span></span>
<span data-ttu-id="c1783-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1783-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1783-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1783-124">-WhatIf</span></span>
<span data-ttu-id="c1783-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1783-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1783-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1783-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1783-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1783-127">CommonParameters</span></span>
<span data-ttu-id="c1783-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1783-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1783-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1783-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1783-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1783-130">INPUTS</span></span>

### <span data-ttu-id="c1783-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c1783-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c1783-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c1783-132">System.String</span></span>

### <span data-ttu-id="c1783-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c1783-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1783-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1783-134">OUTPUTS</span></span>

### <span data-ttu-id="c1783-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1783-135">System.Boolean</span></span>

## <span data-ttu-id="c1783-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1783-136">NOTES</span></span>

## <span data-ttu-id="c1783-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1783-137">RELATED LINKS</span></span>

[<span data-ttu-id="c1783-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c1783-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="c1783-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c1783-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="c1783-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c1783-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


