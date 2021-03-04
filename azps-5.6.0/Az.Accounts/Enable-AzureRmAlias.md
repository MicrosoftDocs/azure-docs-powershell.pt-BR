---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: e99d7643fe67d4102e9f4eef7f9c10f131594948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892674"
---
# <span data-ttu-id="3b0c0-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="3b0c0-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="3b0c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3b0c0-103">Habilita aliases de prefixo do AzureRm para módulos do Az.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="3b0c0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3b0c0-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b0c0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3b0c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3b0c0-106">Habilita aliases de prefixo do AzureRm para módulos do Az.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="3b0c0-107">Se -Module for especificado, somente os módulos listados terão aliases habilitados.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="3b0c0-108">Caso contrário, todos os aliases do AzureRm estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="3b0c0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-109">EXAMPLES</span></span>

### <span data-ttu-id="3b0c0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b0c0-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="3b0c0-111">Habilita todos os prefixos do AzureRm para a sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="3b0c0-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3b0c0-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="3b0c0-113">Habilita aliases do AzureRm para o módulo Az.Accounts para o processo atual e para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="3b0c0-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-114">PARAMETERS</span></span>

### <span data-ttu-id="3b0c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b0c0-115">-DefaultProfile</span></span>
<span data-ttu-id="3b0c0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b0c0-117">-Module</span><span class="sxs-lookup"><span data-stu-id="3b0c0-117">-Module</span></span>
<span data-ttu-id="3b0c0-118">Indica para quais módulos habilitar aliases.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="3b0c0-119">Se nenhum for especificado, o padrão será todos os módulos.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="3b0c0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b0c0-120">-PassThru</span></span>
<span data-ttu-id="3b0c0-121">Se especificado, o cmdlet retornará todos os aliases habilitados</span><span class="sxs-lookup"><span data-stu-id="3b0c0-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="3b0c0-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="3b0c0-122">-Scope</span></span>
<span data-ttu-id="3b0c0-123">Indica para que aliases de escopo devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="3b0c0-124">O padrão é 'Local'</span><span class="sxs-lookup"><span data-stu-id="3b0c0-124">Default is 'Local'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Process, CurrentUser, LocalMachine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b0c0-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b0c0-125">-Confirm</span></span>
<span data-ttu-id="3b0c0-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b0c0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b0c0-127">-WhatIf</span></span>
<span data-ttu-id="3b0c0-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b0c0-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b0c0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b0c0-130">CommonParameters</span></span>
<span data-ttu-id="3b0c0-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b0c0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b0c0-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b0c0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b0c0-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-133">INPUTS</span></span>

### <span data-ttu-id="3b0c0-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3b0c0-134">None</span></span>

## <span data-ttu-id="3b0c0-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-135">OUTPUTS</span></span>

### <span data-ttu-id="3b0c0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3b0c0-136">System.String</span></span>

## <span data-ttu-id="3b0c0-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="3b0c0-137">NOTES</span></span>

## <span data-ttu-id="3b0c0-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b0c0-138">RELATED LINKS</span></span>
