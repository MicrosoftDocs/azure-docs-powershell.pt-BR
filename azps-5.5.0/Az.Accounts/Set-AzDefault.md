---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 25fd0e1cd651f70fa0900c528f9e5297a8eaf2df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110847"
---
# <span data-ttu-id="a60a9-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="a60a9-101">Set-AzDefault</span></span>

## <span data-ttu-id="a60a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a60a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a60a9-103">Define um padrão no contexto atual</span><span class="sxs-lookup"><span data-stu-id="a60a9-103">Sets a default in the current context</span></span>

## <span data-ttu-id="a60a9-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a60a9-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60a9-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a60a9-105">DESCRIPTION</span></span>
<span data-ttu-id="a60a9-106">O Set-AzDefault cmdlet adiciona ou altera os padrões no contexto atual.</span><span class="sxs-lookup"><span data-stu-id="a60a9-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="a60a9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a60a9-107">EXAMPLES</span></span>

### <span data-ttu-id="a60a9-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a60a9-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="a60a9-109">Esse comando define o grupo de recursos padrão para o grupo de recursos especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a60a9-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="a60a9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a60a9-110">PARAMETERS</span></span>

### <span data-ttu-id="a60a9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60a9-111">-DefaultProfile</span></span>
<span data-ttu-id="a60a9-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="a60a9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60a9-113">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a60a9-113">-Force</span></span>
<span data-ttu-id="a60a9-114">Criar um novo grupo de recursos se o padrão especificado não existir</span><span class="sxs-lookup"><span data-stu-id="a60a9-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="a60a9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60a9-115">-ResourceGroupName</span></span>
<span data-ttu-id="a60a9-116">Nome do grupo de recursos que está sendo definido como padrão</span><span class="sxs-lookup"><span data-stu-id="a60a9-116">Name of the resource group being set as default</span></span>

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

### <span data-ttu-id="a60a9-117">-Escopo</span><span class="sxs-lookup"><span data-stu-id="a60a9-117">-Scope</span></span>
<span data-ttu-id="a60a9-118">Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário.</span><span class="sxs-lookup"><span data-stu-id="a60a9-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a60a9-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a60a9-119">-Confirm</span></span>
<span data-ttu-id="a60a9-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60a9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60a9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60a9-121">-WhatIf</span></span>
<span data-ttu-id="a60a9-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a60a9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a60a9-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a60a9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60a9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60a9-124">CommonParameters</span></span>
<span data-ttu-id="a60a9-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60a9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60a9-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60a9-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60a9-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="a60a9-127">INPUTS</span></span>

### <span data-ttu-id="a60a9-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a60a9-128">System.String</span></span>

## <span data-ttu-id="a60a9-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="a60a9-129">OUTPUTS</span></span>

### <span data-ttu-id="a60a9-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a60a9-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="a60a9-131">Notas</span><span class="sxs-lookup"><span data-stu-id="a60a9-131">NOTES</span></span>

## <span data-ttu-id="a60a9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a60a9-132">RELATED LINKS</span></span>
