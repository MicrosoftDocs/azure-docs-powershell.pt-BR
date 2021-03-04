---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 0db56d65893c9c003261c2004435c5d231c014f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890321"
---
# <span data-ttu-id="52577-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="52577-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="52577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52577-102">SYNOPSIS</span></span>
<span data-ttu-id="52577-103">Remove uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="52577-103">Removes an existing operation.</span></span>

## <span data-ttu-id="52577-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="52577-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52577-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="52577-105">DESCRIPTION</span></span>
<span data-ttu-id="52577-106">O cmdlet **Remove-AzApiManagementOperation** remove uma operação existente.</span><span class="sxs-lookup"><span data-stu-id="52577-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="52577-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52577-107">EXAMPLES</span></span>

### <span data-ttu-id="52577-108">Exemplo 1: Remover uma operação de API existente</span><span class="sxs-lookup"><span data-stu-id="52577-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="52577-109">Este comando remove uma operação de API existente.</span><span class="sxs-lookup"><span data-stu-id="52577-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="52577-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="52577-110">PARAMETERS</span></span>

### <span data-ttu-id="52577-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="52577-111">-ApiId</span></span>
<span data-ttu-id="52577-112">Especifica o identificador da API.</span><span class="sxs-lookup"><span data-stu-id="52577-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="52577-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="52577-113">-ApiRevision</span></span>
<span data-ttu-id="52577-114">Identificador da Revisão da API.</span><span class="sxs-lookup"><span data-stu-id="52577-114">Identifier of API Revision.</span></span> <span data-ttu-id="52577-115">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="52577-115">This parameter is optional.</span></span> <span data-ttu-id="52577-116">Se não for especificada, a operação será removida da revisão da api ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="52577-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52577-117">-Context</span><span class="sxs-lookup"><span data-stu-id="52577-117">-Context</span></span>
<span data-ttu-id="52577-118">Especifica uma instância de **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="52577-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="52577-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52577-119">-DefaultProfile</span></span>
<span data-ttu-id="52577-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="52577-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52577-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="52577-121">-OperationId</span></span>
<span data-ttu-id="52577-122">Especifica o identificador da operação da API.</span><span class="sxs-lookup"><span data-stu-id="52577-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="52577-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52577-123">-PassThru</span></span>
<span data-ttu-id="52577-124">Indica que esse cmdlet retornará um valor de $True se tiver êxito ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="52577-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="52577-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52577-125">-Confirm</span></span>
<span data-ttu-id="52577-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52577-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52577-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52577-127">-WhatIf</span></span>
<span data-ttu-id="52577-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="52577-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52577-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="52577-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52577-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52577-130">CommonParameters</span></span>
<span data-ttu-id="52577-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52577-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52577-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52577-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52577-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="52577-133">INPUTS</span></span>

### <span data-ttu-id="52577-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52577-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52577-135">System.String</span><span class="sxs-lookup"><span data-stu-id="52577-135">System.String</span></span>

### <span data-ttu-id="52577-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="52577-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="52577-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="52577-137">OUTPUTS</span></span>

### <span data-ttu-id="52577-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="52577-138">System.Boolean</span></span>

## <span data-ttu-id="52577-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="52577-139">NOTES</span></span>

## <span data-ttu-id="52577-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52577-140">RELATED LINKS</span></span>

[<span data-ttu-id="52577-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="52577-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="52577-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="52577-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="52577-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="52577-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


