---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: ac017af710531ff3294f858a8f95ad7529cd1c11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890324"
---
# <span data-ttu-id="66c5e-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="66c5e-101">Clear-AzDefault</span></span>

## <span data-ttu-id="66c5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="66c5e-103">Limpa os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="66c5e-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="66c5e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="66c5e-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c5e-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="66c5e-105">DESCRIPTION</span></span>
<span data-ttu-id="66c5e-106">O Clear-AzDefault cmdlet remove os padrões definidos pelo usuário, dependendo dos parâmetros de comutadores especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="66c5e-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="66c5e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="66c5e-107">EXAMPLES</span></span>

### <span data-ttu-id="66c5e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="66c5e-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="66c5e-109">Este comando remove todos os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="66c5e-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="66c5e-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="66c5e-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="66c5e-111">Este comando remove o grupo de recursos padrão definido pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="66c5e-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="66c5e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="66c5e-112">PARAMETERS</span></span>

### <span data-ttu-id="66c5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c5e-113">-DefaultProfile</span></span>
<span data-ttu-id="66c5e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="66c5e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c5e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="66c5e-115">-Force</span></span>
<span data-ttu-id="66c5e-116">Remover todos os padrões se nenhum padrão for especificado</span><span class="sxs-lookup"><span data-stu-id="66c5e-116">Remove all defaults if no default is specified</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c5e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66c5e-117">-PassThru</span></span>
<span data-ttu-id="66c5e-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="66c5e-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c5e-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="66c5e-119">-ResourceGroup</span></span>
<span data-ttu-id="66c5e-120">Limpar Grupo de Recursos Padrão</span><span class="sxs-lookup"><span data-stu-id="66c5e-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="66c5e-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="66c5e-121">-Scope</span></span>
<span data-ttu-id="66c5e-122">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="66c5e-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c5e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66c5e-123">-Confirm</span></span>
<span data-ttu-id="66c5e-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66c5e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c5e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c5e-125">-WhatIf</span></span>
<span data-ttu-id="66c5e-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="66c5e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c5e-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="66c5e-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66c5e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c5e-128">CommonParameters</span></span>
<span data-ttu-id="66c5e-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66c5e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c5e-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66c5e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c5e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66c5e-131">INPUTS</span></span>

### <span data-ttu-id="66c5e-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66c5e-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66c5e-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="66c5e-133">OUTPUTS</span></span>

### <span data-ttu-id="66c5e-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66c5e-134">System.Boolean</span></span>

## <span data-ttu-id="66c5e-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="66c5e-135">NOTES</span></span>

## <span data-ttu-id="66c5e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66c5e-136">RELATED LINKS</span></span>
