---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementOperation.md
ms.openlocfilehash: 685da9955f272066ec39890ea0f3a063d3b2f9b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428015"
---
# <span data-ttu-id="c30a7-101">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c30a7-101">Remove-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="c30a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c30a7-102">SYNOPSIS</span></span>
<span data-ttu-id="c30a7-103">Remove uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="c30a7-103">Removes an existing operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c30a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c30a7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c30a7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c30a7-105">DESCRIPTION</span></span>
<span data-ttu-id="c30a7-106">O cmdlet **Remove-AzureRmApiManagementOperation** remove uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="c30a7-106">The **Remove-AzureRmApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="c30a7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c30a7-107">EXAMPLES</span></span>

### <span data-ttu-id="c30a7-108">Exemplo 1: remover uma operação de API existente</span><span class="sxs-lookup"><span data-stu-id="c30a7-108">Example 1: Remove an existing API Operation</span></span>
```
PS C:\>Remove-AzureRmApiManagementOperation -Context $APImContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="c30a7-109">Esse comando Remove uma operação de API existente.</span><span class="sxs-lookup"><span data-stu-id="c30a7-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="c30a7-110">OS</span><span class="sxs-lookup"><span data-stu-id="c30a7-110">PARAMETERS</span></span>

### <span data-ttu-id="c30a7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c30a7-111">-ApiId</span></span>
<span data-ttu-id="c30a7-112">Especifica o identificador da API.</span><span class="sxs-lookup"><span data-stu-id="c30a7-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="c30a7-113">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c30a7-113">-Context</span></span>
<span data-ttu-id="c30a7-114">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="c30a7-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="c30a7-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c30a7-115">-OperationId</span></span>
<span data-ttu-id="c30a7-116">Especifica o identificador da operação de API.</span><span class="sxs-lookup"><span data-stu-id="c30a7-116">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="c30a7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c30a7-117">-PassThru</span></span>
<span data-ttu-id="c30a7-118">Indica que esse cmdlet retorna um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c30a7-118">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="c30a7-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c30a7-119">-Confirm</span></span>
<span data-ttu-id="c30a7-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c30a7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c30a7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c30a7-121">-WhatIf</span></span>
<span data-ttu-id="c30a7-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c30a7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c30a7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c30a7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c30a7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30a7-124">-DefaultProfile</span></span>
<span data-ttu-id="c30a7-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c30a7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c30a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30a7-126">CommonParameters</span></span>
<span data-ttu-id="c30a7-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c30a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30a7-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c30a7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30a7-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c30a7-129">INPUTS</span></span>

## <span data-ttu-id="c30a7-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c30a7-130">OUTPUTS</span></span>

### <span data-ttu-id="c30a7-131">bool</span><span class="sxs-lookup"><span data-stu-id="c30a7-131">bool</span></span>

## <span data-ttu-id="c30a7-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c30a7-132">NOTES</span></span>

## <span data-ttu-id="c30a7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c30a7-133">RELATED LINKS</span></span>

[<span data-ttu-id="c30a7-134">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c30a7-134">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="c30a7-135">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c30a7-135">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="c30a7-136">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c30a7-136">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


