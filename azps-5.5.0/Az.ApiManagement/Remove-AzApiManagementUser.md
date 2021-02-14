---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111225"
---
# <span data-ttu-id="99ae4-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="99ae4-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="99ae4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="99ae4-103">Exclui um usuário existente.</span><span class="sxs-lookup"><span data-stu-id="99ae4-103">Deletes an existing user.</span></span>

## <span data-ttu-id="99ae4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99ae4-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ae4-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="99ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="99ae4-106">O cmdlet **Remove-AzApiManagementUser** exclui um usuário existente.</span><span class="sxs-lookup"><span data-stu-id="99ae4-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="99ae4-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="99ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="99ae4-108">Exemplo 1: Excluir um usuário</span><span class="sxs-lookup"><span data-stu-id="99ae4-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="99ae4-109">Esse comando exclui um usuário existente.</span><span class="sxs-lookup"><span data-stu-id="99ae4-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="99ae4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99ae4-110">PARAMETERS</span></span>

### <span data-ttu-id="99ae4-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="99ae4-111">-Context</span></span>
<span data-ttu-id="99ae4-112">Especifica um **objeto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="99ae4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="99ae4-113">Esse parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="99ae4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="99ae4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ae4-114">-DefaultProfile</span></span>
<span data-ttu-id="99ae4-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="99ae4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99ae4-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="99ae4-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="99ae4-117">Indica se você deve excluir assinaturas do produto.</span><span class="sxs-lookup"><span data-stu-id="99ae4-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="99ae4-118">Se esse parâmetro não for especificado e uma assinatura existir, esse cmdlet lançará uma exceção.</span><span class="sxs-lookup"><span data-stu-id="99ae4-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="99ae4-119">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="99ae4-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="99ae4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99ae4-120">-PassThru</span></span>
<span data-ttu-id="99ae4-121">Indica que esse cmdlet retorna um valor de $Ture, se for bem-sucedido, ou um valor de $False, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="99ae4-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="99ae4-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="99ae4-122">-UserId</span></span>
<span data-ttu-id="99ae4-123">Especifica a ID do usuário a ser removido.</span><span class="sxs-lookup"><span data-stu-id="99ae4-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="99ae4-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="99ae4-124">-Confirm</span></span>
<span data-ttu-id="99ae4-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99ae4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ae4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99ae4-126">-WhatIf</span></span>
<span data-ttu-id="99ae4-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="99ae4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ae4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99ae4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ae4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ae4-129">CommonParameters</span></span>
<span data-ttu-id="99ae4-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ae4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ae4-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99ae4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ae4-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="99ae4-132">INPUTS</span></span>

### <span data-ttu-id="99ae4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="99ae4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="99ae4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="99ae4-134">System.String</span></span>

### <span data-ttu-id="99ae4-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="99ae4-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="99ae4-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="99ae4-136">OUTPUTS</span></span>

### <span data-ttu-id="99ae4-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="99ae4-137">System.Boolean</span></span>

## <span data-ttu-id="99ae4-138">Notas</span><span class="sxs-lookup"><span data-stu-id="99ae4-138">NOTES</span></span>

## <span data-ttu-id="99ae4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99ae4-139">RELATED LINKS</span></span>

[<span data-ttu-id="99ae4-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="99ae4-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="99ae4-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="99ae4-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="99ae4-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="99ae4-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


