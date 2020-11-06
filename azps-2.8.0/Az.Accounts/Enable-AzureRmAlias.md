---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzureRmAlias.md
ms.openlocfilehash: 24862931e19d0e8b8c7b8568aabb6f25cf65f9c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598262"
---
# <span data-ttu-id="085e2-101">Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="085e2-101">Enable-AzureRmAlias</span></span>

## <span data-ttu-id="085e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="085e2-102">SYNOPSIS</span></span>
<span data-ttu-id="085e2-103">Habilita os aliases de prefixo AzureRm para módulos AZ.</span><span class="sxs-lookup"><span data-stu-id="085e2-103">Enables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="085e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="085e2-104">SYNTAX</span></span>

```
Enable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="085e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="085e2-105">DESCRIPTION</span></span>
<span data-ttu-id="085e2-106">Habilita os aliases de prefixo AzureRm para módulos AZ.</span><span class="sxs-lookup"><span data-stu-id="085e2-106">Enables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="085e2-107">Se-Module for especificado, somente os módulos listados terão aliases habilitados.</span><span class="sxs-lookup"><span data-stu-id="085e2-107">If -Module is specified, only modules listed will have aliases enabled.</span></span> <span data-ttu-id="085e2-108">Caso contrário, todos os aliases do AzureRm são habilitados.</span><span class="sxs-lookup"><span data-stu-id="085e2-108">Otherwise all AzureRm aliases are enabled.</span></span>

## <span data-ttu-id="085e2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="085e2-109">EXAMPLES</span></span>

### <span data-ttu-id="085e2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="085e2-110">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias
```

<span data-ttu-id="085e2-111">Habilita todos os prefixos AzureRm para a sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="085e2-111">Enables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="085e2-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="085e2-112">Example 1</span></span>
```
PS C:\> Enable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="085e2-113">Habilita aliases AzureRm para o módulo AZ. Accounts para o processo atual e para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="085e2-113">Enables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="085e2-114">OS</span><span class="sxs-lookup"><span data-stu-id="085e2-114">PARAMETERS</span></span>

### <span data-ttu-id="085e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="085e2-115">-DefaultProfile</span></span>
<span data-ttu-id="085e2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="085e2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="085e2-117">-Módulo</span><span class="sxs-lookup"><span data-stu-id="085e2-117">-Module</span></span>
<span data-ttu-id="085e2-118">Indica os módulos para os quais habilitar aliases.</span><span class="sxs-lookup"><span data-stu-id="085e2-118">Indicates which modules to enable aliases for.</span></span>
<span data-ttu-id="085e2-119">Se nenhum for especificado, o padrão será todos os módulos.</span><span class="sxs-lookup"><span data-stu-id="085e2-119">If none are specified, default is all modules.</span></span>

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

### <span data-ttu-id="085e2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="085e2-120">-PassThru</span></span>
<span data-ttu-id="085e2-121">Se especificado, o cmdlet retornará todos os alias habilitados</span><span class="sxs-lookup"><span data-stu-id="085e2-121">If specified, cmdlet will return all aliases enabled</span></span>

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

### <span data-ttu-id="085e2-122">-Escopo</span><span class="sxs-lookup"><span data-stu-id="085e2-122">-Scope</span></span>
<span data-ttu-id="085e2-123">Indica a que aliases de escopo devem ser habilitados.</span><span class="sxs-lookup"><span data-stu-id="085e2-123">Indicates what scope aliases should be enabled for.</span></span> <span data-ttu-id="085e2-124">O padrão é ' local '</span><span class="sxs-lookup"><span data-stu-id="085e2-124">Default is 'Local'</span></span>

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

### <span data-ttu-id="085e2-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="085e2-125">-Confirm</span></span>
<span data-ttu-id="085e2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="085e2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="085e2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="085e2-127">-WhatIf</span></span>
<span data-ttu-id="085e2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="085e2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="085e2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="085e2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="085e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="085e2-130">CommonParameters</span></span>
<span data-ttu-id="085e2-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="085e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="085e2-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="085e2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="085e2-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="085e2-133">INPUTS</span></span>

### <span data-ttu-id="085e2-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="085e2-134">None</span></span>

## <span data-ttu-id="085e2-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="085e2-135">OUTPUTS</span></span>

### <span data-ttu-id="085e2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="085e2-136">System.String</span></span>

## <span data-ttu-id="085e2-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="085e2-137">NOTES</span></span>

## <span data-ttu-id="085e2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="085e2-138">RELATED LINKS</span></span>
