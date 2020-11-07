---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azurermalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzureRmAlias.md
ms.openlocfilehash: e87c28627c42d75687569d23a0667f5c403a5def
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775267"
---
# <span data-ttu-id="f1ff7-101">Disable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="f1ff7-101">Disable-AzureRmAlias</span></span>

## <span data-ttu-id="f1ff7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f1ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ff7-103">Desabilita os aliases de prefixo AzureRm para módulos AZ.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-103">Disables AzureRm prefix aliases for Az modules.</span></span>

## <span data-ttu-id="f1ff7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1ff7-104">SYNTAX</span></span>

```
Disable-AzureRmAlias [-Scope <String>] [-Module <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ff7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f1ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ff7-106">Desabilita os aliases de prefixo AzureRm para módulos AZ.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-106">Disables AzureRm prefix aliases for Az modules.</span></span> <span data-ttu-id="f1ff7-107">Se-Module for especificado, somente os módulos listados terão aliases desabilitados.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-107">If -Module is specified, only modules listed will have aliases disabled.</span></span> <span data-ttu-id="f1ff7-108">Caso contrário, todos os aliases do AzureRm são desativados.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-108">Otherwise all AzureRm aliases are disabled.</span></span>

## <span data-ttu-id="f1ff7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f1ff7-109">EXAMPLES</span></span>

### <span data-ttu-id="f1ff7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1ff7-110">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias
```

<span data-ttu-id="f1ff7-111">Desabilita todos os prefixos AzureRm para a sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-111">Disables all AzureRm prefixes for the current PowerShell session.</span></span>

### <span data-ttu-id="f1ff7-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f1ff7-112">Example 1</span></span>
```
PS C:\> Disable-AzureRmAlias -Module Az.Accounts -Scope CurrentUser
```

<span data-ttu-id="f1ff7-113">Desabilita os aliases do AzureRm para o módulo AZ. Accounts para o processo atual e para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-113">Disables AzureRm aliases for the Az.Accounts module for both the current process and for the current user.</span></span>

## <span data-ttu-id="f1ff7-114">OS</span><span class="sxs-lookup"><span data-stu-id="f1ff7-114">PARAMETERS</span></span>

### <span data-ttu-id="f1ff7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ff7-115">-DefaultProfile</span></span>
<span data-ttu-id="f1ff7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1ff7-117">-Módulo</span><span class="sxs-lookup"><span data-stu-id="f1ff7-117">-Module</span></span>
<span data-ttu-id="f1ff7-118">Indica os módulos para os quais desabilitar aliases.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-118">Indicates which modules to disable aliases for.</span></span>
<span data-ttu-id="f1ff7-119">Se nenhum for especificado, o padrão será todos os módulos habilitados.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-119">If none are specified, default is all enabled modules.</span></span>

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

### <span data-ttu-id="f1ff7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1ff7-120">-PassThru</span></span>
<span data-ttu-id="f1ff7-121">Se especificado, o cmdlet retornará todos os aliases desabilitados</span><span class="sxs-lookup"><span data-stu-id="f1ff7-121">If specified, cmdlet will return all disabled aliases</span></span>

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

### <span data-ttu-id="f1ff7-122">-Escopo</span><span class="sxs-lookup"><span data-stu-id="f1ff7-122">-Scope</span></span>
<span data-ttu-id="f1ff7-123">Indica quais aliases de escopo devem ser desabilitados.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-123">Indicates what scope aliases should be disabled for.</span></span> <span data-ttu-id="f1ff7-124">O padrão é ' processo '</span><span class="sxs-lookup"><span data-stu-id="f1ff7-124">Default is 'Process'</span></span>

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

### <span data-ttu-id="f1ff7-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f1ff7-125">-Confirm</span></span>
<span data-ttu-id="f1ff7-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ff7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ff7-127">-WhatIf</span></span>
<span data-ttu-id="f1ff7-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ff7-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ff7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ff7-130">CommonParameters</span></span>
<span data-ttu-id="f1ff7-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ff7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ff7-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1ff7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ff7-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f1ff7-133">INPUTS</span></span>

### <span data-ttu-id="f1ff7-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f1ff7-134">None</span></span>

## <span data-ttu-id="f1ff7-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f1ff7-135">OUTPUTS</span></span>

### <span data-ttu-id="f1ff7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f1ff7-136">System.String</span></span>

## <span data-ttu-id="f1ff7-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f1ff7-137">NOTES</span></span>

## <span data-ttu-id="f1ff7-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f1ff7-138">RELATED LINKS</span></span>
