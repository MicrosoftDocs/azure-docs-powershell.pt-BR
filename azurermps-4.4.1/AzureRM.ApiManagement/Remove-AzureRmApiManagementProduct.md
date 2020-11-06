---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427029"
---
# <span data-ttu-id="2890a-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2890a-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="2890a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2890a-102">SYNOPSIS</span></span>
<span data-ttu-id="2890a-103">Remove um produto de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="2890a-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2890a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2890a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2890a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2890a-105">DESCRIPTION</span></span>
<span data-ttu-id="2890a-106">O cmdlet **Remove-AzureRmApiManagementProduct** remove um produto de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="2890a-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="2890a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2890a-107">EXAMPLES</span></span>

### <span data-ttu-id="2890a-108">Exemplo 1: remover um produto existente e todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="2890a-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="2890a-109">Este comando Remove um produto existente e todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="2890a-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="2890a-110">OS</span><span class="sxs-lookup"><span data-stu-id="2890a-110">PARAMETERS</span></span>

### <span data-ttu-id="2890a-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="2890a-111">-Context</span></span>
<span data-ttu-id="2890a-112">Especifica uma instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2890a-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2890a-113">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="2890a-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="2890a-114">Indica se as assinaturas devem ser excluídas do produto.</span><span class="sxs-lookup"><span data-stu-id="2890a-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="2890a-115">Se você não definir esse parâmetro e as assinaturas existirem, uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="2890a-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="2890a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2890a-116">-PassThru</span></span>
<span data-ttu-id="2890a-117">Indica que esse cmdlet retorna um valor de $True, se tiver êxito ou um valor de $False, se falhar.</span><span class="sxs-lookup"><span data-stu-id="2890a-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="2890a-118">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2890a-118">-ProductId</span></span>
<span data-ttu-id="2890a-119">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="2890a-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="2890a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2890a-120">-Confirm</span></span>
<span data-ttu-id="2890a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2890a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2890a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2890a-122">-WhatIf</span></span>
<span data-ttu-id="2890a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2890a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2890a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2890a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2890a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2890a-125">-DefaultProfile</span></span>
<span data-ttu-id="2890a-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2890a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2890a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2890a-127">CommonParameters</span></span>
<span data-ttu-id="2890a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2890a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2890a-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2890a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2890a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2890a-130">INPUTS</span></span>

## <span data-ttu-id="2890a-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2890a-131">OUTPUTS</span></span>

### <span data-ttu-id="2890a-132">bool</span><span class="sxs-lookup"><span data-stu-id="2890a-132">bool</span></span>

## <span data-ttu-id="2890a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2890a-133">NOTES</span></span>

## <span data-ttu-id="2890a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2890a-134">RELATED LINKS</span></span>

[<span data-ttu-id="2890a-135">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2890a-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="2890a-136">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2890a-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="2890a-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2890a-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


