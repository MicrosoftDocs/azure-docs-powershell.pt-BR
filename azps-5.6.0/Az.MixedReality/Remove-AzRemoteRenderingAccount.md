---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: ef14039cc1f46c3a891090475814d6e9553da431
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892469"
---
# <span data-ttu-id="56828-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="56828-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="56828-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56828-102">SYNOPSIS</span></span>
<span data-ttu-id="56828-103">Excluir conta de renderização remota</span><span class="sxs-lookup"><span data-stu-id="56828-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="56828-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56828-104">SYNTAX</span></span>

### <span data-ttu-id="56828-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56828-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56828-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56828-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56828-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="56828-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56828-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56828-108">DESCRIPTION</span></span>
<span data-ttu-id="56828-109">Exclua a Conta de Renderização Remota especificada de determinado Grupo de Recursos e Assinaturas.</span><span class="sxs-lookup"><span data-stu-id="56828-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="56828-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56828-110">EXAMPLES</span></span>

### <span data-ttu-id="56828-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56828-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="56828-112">Exclua a conta de renderização remota "example" do grupo de recursos e assinatura atual "rg1".</span><span class="sxs-lookup"><span data-stu-id="56828-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="56828-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56828-113">PARAMETERS</span></span>

### <span data-ttu-id="56828-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56828-114">-Confirm</span></span>
<span data-ttu-id="56828-115">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56828-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56828-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56828-116">-DefaultProfile</span></span>
<span data-ttu-id="56828-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56828-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56828-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56828-118">-InputObject</span></span>
<span data-ttu-id="56828-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="56828-119">The custom domain object.</span></span>

```yaml
Type: PSRemoteRenderingAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56828-120">-Name</span><span class="sxs-lookup"><span data-stu-id="56828-120">-Name</span></span>
<span data-ttu-id="56828-121">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="56828-121">Remote Rendering Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: RemoteRenderingAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56828-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56828-122">-PassThru</span></span>
<span data-ttu-id="56828-123">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="56828-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56828-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56828-124">-ResourceGroupName</span></span>
<span data-ttu-id="56828-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="56828-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56828-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56828-126">-ResourceId</span></span>
<span data-ttu-id="56828-127">ID de recurso da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="56828-127">Resource ID of Remote Rendering Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56828-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56828-128">-WhatIf</span></span>
<span data-ttu-id="56828-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56828-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56828-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56828-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56828-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56828-131">CommonParameters</span></span>
<span data-ttu-id="56828-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56828-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="56828-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56828-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56828-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56828-134">INPUTS</span></span>

### <span data-ttu-id="56828-135">System.String</span><span class="sxs-lookup"><span data-stu-id="56828-135">System.String</span></span>

### <span data-ttu-id="56828-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="56828-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="56828-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="56828-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="56828-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56828-138">OUTPUTS</span></span>

### <span data-ttu-id="56828-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="56828-139">System.Boolean</span></span>

## <span data-ttu-id="56828-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="56828-140">NOTES</span></span>

## <span data-ttu-id="56828-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56828-141">RELATED LINKS</span></span>
