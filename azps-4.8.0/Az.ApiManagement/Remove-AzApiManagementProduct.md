---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955800"
---
# <span data-ttu-id="40e51-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40e51-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="40e51-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40e51-102">SYNOPSIS</span></span>
<span data-ttu-id="40e51-103">Remove um produto de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="40e51-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="40e51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40e51-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e51-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40e51-105">DESCRIPTION</span></span>
<span data-ttu-id="40e51-106">O cmdlet **Remove-AzApiManagementProduct** remove um produto de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="40e51-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="40e51-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40e51-107">EXAMPLES</span></span>

### <span data-ttu-id="40e51-108">Exemplo 1: remover um produto existente e todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="40e51-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="40e51-109">Este comando Remove um produto existente e todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="40e51-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="40e51-110">OS</span><span class="sxs-lookup"><span data-stu-id="40e51-110">PARAMETERS</span></span>

### <span data-ttu-id="40e51-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="40e51-111">-Context</span></span>
<span data-ttu-id="40e51-112">Especifica uma instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="40e51-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40e51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e51-113">-DefaultProfile</span></span>
<span data-ttu-id="40e51-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40e51-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40e51-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="40e51-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="40e51-116">Indica se as assinaturas devem ser excluídas do produto.</span><span class="sxs-lookup"><span data-stu-id="40e51-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="40e51-117">Se você não definir esse parâmetro e as assinaturas existirem, uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="40e51-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="40e51-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40e51-118">-PassThru</span></span>
<span data-ttu-id="40e51-119">Indica que esse cmdlet retorna um valor de $True, se tiver êxito ou um valor de $False, se falhar.</span><span class="sxs-lookup"><span data-stu-id="40e51-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="40e51-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="40e51-120">-ProductId</span></span>
<span data-ttu-id="40e51-121">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="40e51-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="40e51-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="40e51-122">-Confirm</span></span>
<span data-ttu-id="40e51-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e51-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40e51-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e51-124">-WhatIf</span></span>
<span data-ttu-id="40e51-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="40e51-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e51-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="40e51-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40e51-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e51-127">CommonParameters</span></span>
<span data-ttu-id="40e51-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e51-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e51-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40e51-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e51-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40e51-130">INPUTS</span></span>

### <span data-ttu-id="40e51-131">Microsoft. Azure. Commands. ApiManagement. onmanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="40e51-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40e51-132">System. String</span><span class="sxs-lookup"><span data-stu-id="40e51-132">System.String</span></span>

### <span data-ttu-id="40e51-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="40e51-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="40e51-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40e51-134">OUTPUTS</span></span>

### <span data-ttu-id="40e51-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40e51-135">System.Boolean</span></span>

## <span data-ttu-id="40e51-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40e51-136">NOTES</span></span>

## <span data-ttu-id="40e51-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40e51-137">RELATED LINKS</span></span>

[<span data-ttu-id="40e51-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40e51-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="40e51-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40e51-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="40e51-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40e51-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


