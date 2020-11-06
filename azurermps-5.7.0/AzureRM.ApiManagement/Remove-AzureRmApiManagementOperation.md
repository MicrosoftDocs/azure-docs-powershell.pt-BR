---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: ef3db99522c07b593493e30bd3778f1774af1a5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440148"
---
# <span data-ttu-id="0e1a0-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0e1a0-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="0e1a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1a0-103">Remove uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e1a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e1a0-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e1a0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e1a0-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1a0-106">O cmdlet **Remove-AzureRmApiManagementOperation** remove uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="0e1a0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e1a0-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1a0-108">Exemplo 1: remover uma operação de API existente</span><span class="sxs-lookup"><span data-stu-id="0e1a0-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="0e1a0-109">Esse comando Remove uma operação de API existente.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="0e1a0-110">OS</span><span class="sxs-lookup"><span data-stu-id="0e1a0-110">PARAMETERS</span></span>

### <span data-ttu-id="0e1a0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0e1a0-111">-ApiId</span></span>
<span data-ttu-id="0e1a0-112">Especifica o identificador da API.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="0e1a0-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0e1a0-113">-Context</span></span>
<span data-ttu-id="0e1a0-114">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="0e1a0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1a0-115">-DefaultProfile</span></span>
<span data-ttu-id="0e1a0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0e1a0-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0e1a0-117">-OperationId</span></span>
<span data-ttu-id="0e1a0-118">Especifica o identificador da operação de API.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-118">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="0e1a0-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e1a0-119">-PassThru</span></span>
<span data-ttu-id="0e1a0-120">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-120">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0e1a0-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0e1a0-121">-Confirm</span></span>
<span data-ttu-id="0e1a0-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e1a0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e1a0-123">-WhatIf</span></span>
<span data-ttu-id="0e1a0-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e1a0-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e1a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1a0-126">CommonParameters</span></span>
<span data-ttu-id="0e1a0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1a0-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1a0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1a0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e1a0-129">INPUTS</span></span>

### <span data-ttu-id="0e1a0-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0e1a0-130">None</span></span>
<span data-ttu-id="0e1a0-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="0e1a0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e1a0-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e1a0-132">OUTPUTS</span></span>

### <span data-ttu-id="0e1a0-133">bool</span><span class="sxs-lookup"><span data-stu-id="0e1a0-133">bool</span></span>

## <span data-ttu-id="0e1a0-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e1a0-134">NOTES</span></span>

## <span data-ttu-id="0e1a0-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e1a0-135">RELATED LINKS</span></span>

[<span data-ttu-id="0e1a0-136">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0e1a0-136">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0e1a0-137">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0e1a0-137">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0e1a0-138">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0e1a0-138">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


