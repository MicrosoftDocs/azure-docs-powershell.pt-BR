---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: 1f9f17e03a9b3cf79b2764c7711da9eee6ca104d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891533"
---
# <span data-ttu-id="06b83-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="06b83-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="06b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06b83-102">SYNOPSIS</span></span>
<span data-ttu-id="06b83-103">Desabilita aliases de prefixo do AzureRm para módulos do Az.</span><span class="sxs-lookup"><span data-stu-id="06b83-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="06b83-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="06b83-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06b83-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="06b83-105">DESCRIPTION</span></span>
<span data-ttu-id="06b83-106">Desabilita aliases de prefixo do AzureRm para módulos do Az.</span><span class="sxs-lookup"><span data-stu-id="06b83-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="06b83-107">Se -Module for especificado, somente os módulos listados terão aliases desabilitados.</span><span class="sxs-lookup"><span data-stu-id="06b83-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="06b83-108">Caso contrário, todos os aliases do AzureRm serão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="06b83-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="06b83-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06b83-109">EXAMPLES</span></span>

### <span data-ttu-id="06b83-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06b83-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="06b83-111">Desabilita todos os prefixos do AzureRm para a sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06b83-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="06b83-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06b83-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="06b83-113">Desabilita aliases do AzureRm para o módulo Az.Accounts para o processo atual e para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="06b83-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="06b83-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="06b83-114">PARAMETERS</span></span>

### <span data-ttu-id="06b83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b83-115">-DefaultProfile</span></span>
<span data-ttu-id="06b83-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06b83-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06b83-117">-Module</span><span class="sxs-lookup"><span data-stu-id="06b83-117">-Module</span></span>
<span data-ttu-id="06b83-118">Indica para quais módulos desabilitar aliases.</span><span class="sxs-lookup"><span data-stu-id="06b83-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="06b83-119">Se nenhum for especificado, o padrão será todos os módulos habilitados.</span><span class="sxs-lookup"><span data-stu-id="06b83-119">If none are specified, default is all enabled modules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b83-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06b83-120">-PassThru</span></span>
<span data-ttu-id="06b83-121">Se especificado, o cmdlet retornará todos os aliases desabilitados</span><span class="sxs-lookup"><span data-stu-id="06b83-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="06b83-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="06b83-122">-Scope</span></span>
<span data-ttu-id="06b83-123">Indica para que aliases de escopo devem ser desabilitados.</span><span class="sxs-lookup"><span data-stu-id="06b83-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="06b83-124">O padrão é 'Process'</span><span class="sxs-lookup"><span data-stu-id="06b83-124">Default is 'Process'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b83-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06b83-125">-Confirm</span></span>
<span data-ttu-id="06b83-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06b83-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06b83-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06b83-127">-WhatIf</span></span>
<span data-ttu-id="06b83-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="06b83-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06b83-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="06b83-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06b83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b83-130">CommonParameters</span></span>
<span data-ttu-id="06b83-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b83-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06b83-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b83-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06b83-133">INPUTS</span></span>

### <span data-ttu-id="06b83-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="06b83-134">None</span></span>

## <span data-ttu-id="06b83-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="06b83-135">OUTPUTS</span></span>

### <span data-ttu-id="06b83-136">System.String</span><span class="sxs-lookup"><span data-stu-id="06b83-136">System.String</span></span>

## <span data-ttu-id="06b83-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="06b83-137">NOTES</span></span>

## <span data-ttu-id="06b83-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06b83-138">RELATED LINKS</span></span>
