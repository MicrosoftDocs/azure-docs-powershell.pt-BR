---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: 41d43bcb1164907bc7a06a7de4477f8a719604eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595820"
---
# <span data-ttu-id="90b39-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="90b39-101">Clear-AzDefault</span></span>

## <span data-ttu-id="90b39-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90b39-102">SYNOPSIS</span></span>
<span data-ttu-id="90b39-103">Limpa os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="90b39-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="90b39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90b39-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b39-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90b39-105">DESCRIPTION</span></span>
<span data-ttu-id="90b39-106">O cmdlet Clear-AzDefault remove os padrões definidos pelo usuário, dependendo dos parâmetros de opção especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="90b39-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="90b39-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90b39-107">EXAMPLES</span></span>

### <span data-ttu-id="90b39-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90b39-108">Example 1</span></span>
```
PS C:\> Clear-AzDefault
```

<span data-ttu-id="90b39-109">Esse comando Remove todos os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="90b39-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="90b39-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90b39-110">Example 1</span></span>
```
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="90b39-111">Esse comando Remove o grupo de recursos padrão definido pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="90b39-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="90b39-112">OS</span><span class="sxs-lookup"><span data-stu-id="90b39-112">PARAMETERS</span></span>

### <span data-ttu-id="90b39-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b39-113">-DefaultProfile</span></span>
<span data-ttu-id="90b39-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90b39-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b39-115">-Force</span><span class="sxs-lookup"><span data-stu-id="90b39-115">-Force</span></span>
<span data-ttu-id="90b39-116">Remover todos os padrões se nenhum padrão for especificado</span><span class="sxs-lookup"><span data-stu-id="90b39-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="90b39-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90b39-117">-PassThru</span></span>
<span data-ttu-id="90b39-118">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="90b39-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="90b39-119">-Resource</span><span class="sxs-lookup"><span data-stu-id="90b39-119">-ResourceGroup</span></span>
<span data-ttu-id="90b39-120">Limpar grupo de recursos padrão</span><span class="sxs-lookup"><span data-stu-id="90b39-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="90b39-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="90b39-121">-Scope</span></span>
<span data-ttu-id="90b39-122">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="90b39-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="90b39-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="90b39-123">-Confirm</span></span>
<span data-ttu-id="90b39-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90b39-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b39-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b39-125">-WhatIf</span></span>
<span data-ttu-id="90b39-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="90b39-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b39-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="90b39-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b39-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b39-128">CommonParameters</span></span>
<span data-ttu-id="90b39-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b39-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b39-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b39-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b39-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90b39-131">INPUTS</span></span>

### <span data-ttu-id="90b39-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90b39-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90b39-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90b39-133">OUTPUTS</span></span>

### <span data-ttu-id="90b39-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90b39-134">System.Boolean</span></span>

## <span data-ttu-id="90b39-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90b39-135">NOTES</span></span>

## <span data-ttu-id="90b39-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90b39-136">RELATED LINKS</span></span>
