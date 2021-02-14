---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: b7ee3110fec96a10388ffb41b0a82647db461f37
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111263"
---
# <span data-ttu-id="9fe11-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="9fe11-101">Clear-AzDefault</span></span>

## <span data-ttu-id="9fe11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fe11-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe11-103">Limpa os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="9fe11-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="9fe11-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9fe11-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe11-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9fe11-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe11-106">O Clear-AzDefault cmdlet remove os padrões definidos pelo usuário dependendo dos parâmetros de opção especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="9fe11-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="9fe11-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9fe11-107">EXAMPLES</span></span>

### <span data-ttu-id="9fe11-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fe11-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="9fe11-109">Esse comando remove todos os padrões definidos pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="9fe11-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="9fe11-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9fe11-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="9fe11-111">Esse comando remove o grupo de recursos padrão definido pelo usuário no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="9fe11-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="9fe11-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fe11-112">PARAMETERS</span></span>

### <span data-ttu-id="9fe11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe11-113">-DefaultProfile</span></span>
<span data-ttu-id="9fe11-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9fe11-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fe11-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="9fe11-115">-Force</span></span>
<span data-ttu-id="9fe11-116">Remover todos os padrões se nenhum padrão for especificado</span><span class="sxs-lookup"><span data-stu-id="9fe11-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="9fe11-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fe11-117">-PassThru</span></span>
<span data-ttu-id="9fe11-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9fe11-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9fe11-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9fe11-119">-ResourceGroup</span></span>
<span data-ttu-id="9fe11-120">Limpar Grupo de Recursos Padrão</span><span class="sxs-lookup"><span data-stu-id="9fe11-120">Clear Default Resource Group</span></span>

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

### <span data-ttu-id="9fe11-121">-Escopo</span><span class="sxs-lookup"><span data-stu-id="9fe11-121">-Scope</span></span>
<span data-ttu-id="9fe11-122">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="9fe11-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="9fe11-123">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9fe11-123">-Confirm</span></span>
<span data-ttu-id="9fe11-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fe11-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe11-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe11-125">-WhatIf</span></span>
<span data-ttu-id="9fe11-126">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9fe11-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe11-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9fe11-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe11-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe11-128">CommonParameters</span></span>
<span data-ttu-id="9fe11-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fe11-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe11-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe11-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe11-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="9fe11-131">INPUTS</span></span>

### <span data-ttu-id="9fe11-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fe11-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9fe11-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="9fe11-133">OUTPUTS</span></span>

### <span data-ttu-id="9fe11-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9fe11-134">System.Boolean</span></span>

## <span data-ttu-id="9fe11-135">Notas</span><span class="sxs-lookup"><span data-stu-id="9fe11-135">NOTES</span></span>

## <span data-ttu-id="9fe11-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fe11-136">RELATED LINKS</span></span>
