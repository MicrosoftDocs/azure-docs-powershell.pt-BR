---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426840"
---
# <span data-ttu-id="aa29c-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="aa29c-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="aa29c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa29c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa29c-103">Remove um produto de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="aa29c-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa29c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa29c-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa29c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa29c-105">DESCRIPTION</span></span>
<span data-ttu-id="aa29c-106">O cmdlet **Remove-AzureRmApiManagementProduct** remove um produto de gerenciamento de API existente.</span><span class="sxs-lookup"><span data-stu-id="aa29c-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="aa29c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa29c-107">EXAMPLES</span></span>

### <span data-ttu-id="aa29c-108">Exemplo 1: remover um produto existente e todas as assinaturas</span><span class="sxs-lookup"><span data-stu-id="aa29c-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="aa29c-109">Este comando Remove um produto existente e todas as assinaturas.</span><span class="sxs-lookup"><span data-stu-id="aa29c-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="aa29c-110">OS</span><span class="sxs-lookup"><span data-stu-id="aa29c-110">PARAMETERS</span></span>

### <span data-ttu-id="aa29c-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="aa29c-111">-Context</span></span>
<span data-ttu-id="aa29c-112">Especifica uma instância do objeto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="aa29c-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa29c-113">-DefaultProfile</span></span>
<span data-ttu-id="aa29c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aa29c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="aa29c-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="aa29c-116">Indica se as assinaturas devem ser excluídas do produto.</span><span class="sxs-lookup"><span data-stu-id="aa29c-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="aa29c-117">Se você não definir esse parâmetro e as assinaturas existirem, uma exceção será lançada.</span><span class="sxs-lookup"><span data-stu-id="aa29c-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa29c-118">-PassThru</span></span>
<span data-ttu-id="aa29c-119">Indica que esse cmdlet retorna um valor de $True, se tiver êxito ou um valor de $False, se falhar.</span><span class="sxs-lookup"><span data-stu-id="aa29c-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="aa29c-120">-ProductId</span></span>
<span data-ttu-id="aa29c-121">Especifica o identificador do produto existente.</span><span class="sxs-lookup"><span data-stu-id="aa29c-121">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="aa29c-122">-Confirm</span></span>
<span data-ttu-id="aa29c-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa29c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa29c-124">-WhatIf</span></span>
<span data-ttu-id="aa29c-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aa29c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa29c-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aa29c-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa29c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa29c-127">CommonParameters</span></span>
<span data-ttu-id="aa29c-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa29c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa29c-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa29c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa29c-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa29c-130">INPUTS</span></span>

### <span data-ttu-id="aa29c-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="aa29c-131">None</span></span>
<span data-ttu-id="aa29c-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="aa29c-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa29c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa29c-133">OUTPUTS</span></span>

### <span data-ttu-id="aa29c-134">bool</span><span class="sxs-lookup"><span data-stu-id="aa29c-134">bool</span></span>

## <span data-ttu-id="aa29c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa29c-135">NOTES</span></span>

## <span data-ttu-id="aa29c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa29c-136">RELATED LINKS</span></span>

[<span data-ttu-id="aa29c-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="aa29c-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="aa29c-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="aa29c-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="aa29c-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="aa29c-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


