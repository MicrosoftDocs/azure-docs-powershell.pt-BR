---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112969"
---
# <span data-ttu-id="f14a4-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="f14a4-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="f14a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f14a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f14a4-103">Excluir Conta de Renderização Remota</span><span class="sxs-lookup"><span data-stu-id="f14a4-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="f14a4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f14a4-104">SYNTAX</span></span>

### <span data-ttu-id="f14a4-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f14a4-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14a4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14a4-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f14a4-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f14a4-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f14a4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f14a4-108">DESCRIPTION</span></span>
<span data-ttu-id="f14a4-109">Exclua a Conta de Renderização Remota especificada de determinado Grupo de Recursos e Assinatura.</span><span class="sxs-lookup"><span data-stu-id="f14a4-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="f14a4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f14a4-110">EXAMPLES</span></span>

### <span data-ttu-id="f14a4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f14a4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="f14a4-112">Exclua "exemplo" de Conta de Renderização Remota da assinatura atual e grupo de recursos "rg1".</span><span class="sxs-lookup"><span data-stu-id="f14a4-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="f14a4-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f14a4-113">PARAMETERS</span></span>

### <span data-ttu-id="f14a4-114">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f14a4-114">-Confirm</span></span>
<span data-ttu-id="f14a4-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f14a4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f14a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14a4-116">-DefaultProfile</span></span>
<span data-ttu-id="f14a4-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f14a4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f14a4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f14a4-118">-InputObject</span></span>
<span data-ttu-id="f14a4-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="f14a4-119">The custom domain object.</span></span>

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

### <span data-ttu-id="f14a4-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f14a4-120">-Name</span></span>
<span data-ttu-id="f14a4-121">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="f14a4-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="f14a4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f14a4-122">-PassThru</span></span>
<span data-ttu-id="f14a4-123">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="f14a4-123">Return object if specified.</span></span>

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

### <span data-ttu-id="f14a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f14a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f14a4-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f14a4-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f14a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f14a4-126">-ResourceId</span></span>
<span data-ttu-id="f14a4-127">ID do Recurso da Conta de Renderização Remota.</span><span class="sxs-lookup"><span data-stu-id="f14a4-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="f14a4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f14a4-128">-WhatIf</span></span>
<span data-ttu-id="f14a4-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f14a4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f14a4-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f14a4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f14a4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f14a4-131">CommonParameters</span></span>
<span data-ttu-id="f14a4-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f14a4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f14a4-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f14a4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f14a4-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="f14a4-134">INPUTS</span></span>

### <span data-ttu-id="f14a4-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f14a4-135">System.String</span></span>

### <span data-ttu-id="f14a4-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoterenderingAccount</span><span class="sxs-lookup"><span data-stu-id="f14a4-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="f14a4-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f14a4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f14a4-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="f14a4-138">OUTPUTS</span></span>

### <span data-ttu-id="f14a4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f14a4-139">System.Boolean</span></span>

## <span data-ttu-id="f14a4-140">Notas</span><span class="sxs-lookup"><span data-stu-id="f14a4-140">NOTES</span></span>

## <span data-ttu-id="f14a4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f14a4-141">RELATED LINKS</span></span>
