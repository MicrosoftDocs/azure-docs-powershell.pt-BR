---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 6a530a0e20f3e69540320ad3eab8b8cc7f37b5af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115575"
---
# <span data-ttu-id="ab837-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ab837-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="ab837-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab837-102">SYNOPSIS</span></span>
<span data-ttu-id="ab837-103">Habilita aliases de prefixo do AzureRm para módulos do Az.</span><span class="sxs-lookup"><span data-stu-id="ab837-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="ab837-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab837-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab837-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab837-105">DESCRIPTION</span></span>
<span data-ttu-id="ab837-106">Habilita aliases de prefixo do AzureRm para módulos do Az.</span><span class="sxs-lookup"><span data-stu-id="ab837-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="ab837-107">Se -Module for especificado, somente os módulos listados terão aliases habilitados.</span><span class="sxs-lookup"><span data-stu-id="ab837-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="ab837-108">Caso contrário, todos os aliases do AzureRm estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="ab837-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="ab837-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab837-109">EXAMPLES</span></span>

### <span data-ttu-id="ab837-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab837-110">Example 1</span></span>
```powershell
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="ab837-111">Habilita todos os prefixos do AzureRm para a sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab837-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="ab837-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ab837-112">Example 2</span></span>
```powershell
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="ab837-113">Habilita aliases do AzureRm para o módulo Az.Accounts para o processo atual e para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ab837-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="ab837-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab837-114">PARAMETERS</span></span>

### <span data-ttu-id="ab837-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab837-115">-DefaultProfile</span></span>
<span data-ttu-id="ab837-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab837-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab837-117">-Module</span><span class="sxs-lookup"><span data-stu-id="ab837-117">-Module</span></span>
<span data-ttu-id="ab837-118">Indica para quais módulos habilitar aliases.</span><span class="sxs-lookup"><span data-stu-id="ab837-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="ab837-119">Se nenhum for especificado, o padrão será todos os módulos.</span><span class="sxs-lookup"><span data-stu-id="ab837-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="ab837-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab837-120">-PassThru</span></span>
<span data-ttu-id="ab837-121">Se especificado, o cmdlet retornará todos os aliases habilitados</span><span class="sxs-lookup"><span data-stu-id="ab837-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="ab837-122">-Escopo</span><span class="sxs-lookup"><span data-stu-id="ab837-122">-Scope</span></span>
<span data-ttu-id="ab837-123">Indica para quais aliases de escopo devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="ab837-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="ab837-124">O padrão é "Local"</span><span class="sxs-lookup"><span data-stu-id="ab837-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="ab837-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ab837-125">-Confirm</span></span>
<span data-ttu-id="ab837-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab837-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab837-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab837-127">-WhatIf</span></span>
<span data-ttu-id="ab837-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ab837-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab837-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab837-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab837-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab837-130">CommonParameters</span></span>
<span data-ttu-id="ab837-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab837-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab837-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab837-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab837-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="ab837-133">INPUTS</span></span>

### <span data-ttu-id="ab837-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ab837-134">None</span></span>

## <span data-ttu-id="ab837-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="ab837-135">OUTPUTS</span></span>

### <span data-ttu-id="ab837-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ab837-136">System.String</span></span>

## <span data-ttu-id="ab837-137">Notas</span><span class="sxs-lookup"><span data-stu-id="ab837-137">NOTES</span></span>

## <span data-ttu-id="ab837-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab837-138">RELATED LINKS</span></span>
