---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azremoterenderingaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzRemoteRenderingAccountKey.md
ms.openlocfilehash: be0e79bbc6d1cd9c2a356852e2d9dea83439d25f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259290"
---
# <span data-ttu-id="fd6c3-101">New-AzRemoteRenderingAccountKey</span><span class="sxs-lookup"><span data-stu-id="fd6c3-101">New-AzRemoteRenderingAccountKey</span></span>

## <span data-ttu-id="fd6c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd6c3-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6c3-103">Regenerar a chave da conta de renderização remota</span><span class="sxs-lookup"><span data-stu-id="fd6c3-103">Regenerate key of Remote Rendering Account</span></span>

## <span data-ttu-id="fd6c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd6c3-104">SYNTAX</span></span>

### <span data-ttu-id="fd6c3-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6c3-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6c3-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6c3-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6c3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6c3-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6c3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6c3-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6c3-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6c3-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd6c3-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd6c3-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzRemoteRenderingAccountKey -InputObject <PSRemoteRenderingAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd6c3-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd6c3-111">DESCRIPTION</span></span>
<span data-ttu-id="fd6c3-112">Regenerar a chave primária ou a chave secundária da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-112">Regenerate primary key or secondary key of Remote Rendering Account.</span></span>

## <span data-ttu-id="fd6c3-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd6c3-113">EXAMPLES</span></span>

### <span data-ttu-id="fd6c3-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fd6c3-114">Example 1</span></span>
```powershell
PS C:\> New-AzRemoteRenderingAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="fd6c3-115">Regenerar a chave secundária da conta de renderização remota "exemplo" no grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="fd6c3-115">Regenerate secondary key of Remote Rendering Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="fd6c3-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fd6c3-116">Example 2</span></span>
```powershell
PS C:\> Get-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example | New-AzRemoteRenderingAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="fd6c3-117">Regenerar a chave secundária da conta de renderização remota "exemplo" da assinatura atual e do grupo de recursos "Rg1" com o encanamento.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-117">Regenerate secondary key of Remote Rendering Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="fd6c3-118">OS</span><span class="sxs-lookup"><span data-stu-id="fd6c3-118">PARAMETERS</span></span>

### <span data-ttu-id="fd6c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd6c3-119">-DefaultProfile</span></span>
<span data-ttu-id="fd6c3-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fd6c3-121">-Force</span></span>
<span data-ttu-id="fd6c3-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd6c3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd6c3-123">-InputObject</span></span>
<span data-ttu-id="fd6c3-124">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-124">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd6c3-125">-Name</span></span>
<span data-ttu-id="fd6c3-126">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-126">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-127">-Principal</span><span class="sxs-lookup"><span data-stu-id="fd6c3-127">-Primary</span></span>
<span data-ttu-id="fd6c3-128">Regenerar a chave primária da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-128">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd6c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="fd6c3-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd6c3-131">-ResourceId</span></span>
<span data-ttu-id="fd6c3-132">ID do recurso da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-132">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-133">-Secundário</span><span class="sxs-lookup"><span data-stu-id="fd6c3-133">-Secondary</span></span>
<span data-ttu-id="fd6c3-134">Regenerar a chave primária da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-134">Regenerate primary key of Remote Rendering Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd6c3-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd6c3-135">-Confirm</span></span>
<span data-ttu-id="fd6c3-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd6c3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd6c3-137">-WhatIf</span></span>
<span data-ttu-id="fd6c3-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd6c3-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd6c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6c3-140">CommonParameters</span></span>
<span data-ttu-id="fd6c3-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd6c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="fd6c3-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd6c3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6c3-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd6c3-143">INPUTS</span></span>

### <span data-ttu-id="fd6c3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fd6c3-144">System.String</span></span>

### <span data-ttu-id="fd6c3-145">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="fd6c3-145">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

## <span data-ttu-id="fd6c3-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd6c3-146">OUTPUTS</span></span>

### <span data-ttu-id="fd6c3-147">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fd6c3-147">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSAccountKeys</span></span>

## <span data-ttu-id="fd6c3-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd6c3-148">NOTES</span></span>

## <span data-ttu-id="fd6c3-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd6c3-149">RELATED LINKS</span></span>
