---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azremoterenderingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzRemoteRenderingAccount.md
ms.openlocfilehash: bfcbaa723dc2d06d74ba4d515affd2f19a51ec3e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259288"
---
# <span data-ttu-id="7086f-101">Remove-AzRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7086f-101">Remove-AzRemoteRenderingAccount</span></span>

## <span data-ttu-id="7086f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7086f-102">SYNOPSIS</span></span>
<span data-ttu-id="7086f-103">Excluir conta de renderização remota</span><span class="sxs-lookup"><span data-stu-id="7086f-103">Delete Remote Rendering Account</span></span>

## <span data-ttu-id="7086f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7086f-104">SYNTAX</span></span>

### <span data-ttu-id="7086f-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7086f-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7086f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7086f-106">ResourceIdParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7086f-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="7086f-107">PipelineParameterSet</span></span>
```
Remove-AzRemoteRenderingAccount -InputObject <PSRemoteRenderingAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7086f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7086f-108">DESCRIPTION</span></span>
<span data-ttu-id="7086f-109">Exclua a conta de renderização remota especificada de determinada assinatura e grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7086f-109">Delete specified Remote Rendering Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="7086f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7086f-110">EXAMPLES</span></span>

### <span data-ttu-id="7086f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7086f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRemoteRenderingAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="7086f-112">Excluir conta de renderização remota "exemplo" da assinatura atual e do grupo de recursos "Rg1".</span><span class="sxs-lookup"><span data-stu-id="7086f-112">Delete Remote Rendering Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="7086f-113">OS</span><span class="sxs-lookup"><span data-stu-id="7086f-113">PARAMETERS</span></span>

### <span data-ttu-id="7086f-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7086f-114">-Confirm</span></span>
<span data-ttu-id="7086f-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7086f-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7086f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7086f-116">-DefaultProfile</span></span>
<span data-ttu-id="7086f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7086f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7086f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7086f-118">-InputObject</span></span>
<span data-ttu-id="7086f-119">O objeto de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="7086f-119">The custom domain object.</span></span>

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

### <span data-ttu-id="7086f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7086f-120">-Name</span></span>
<span data-ttu-id="7086f-121">Nome da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="7086f-121">Remote Rendering Account Name.</span></span>

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

### <span data-ttu-id="7086f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7086f-122">-PassThru</span></span>
<span data-ttu-id="7086f-123">Objeto de retorno, se especificado.</span><span class="sxs-lookup"><span data-stu-id="7086f-123">Return object if specified.</span></span>

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

### <span data-ttu-id="7086f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7086f-124">-ResourceGroupName</span></span>
<span data-ttu-id="7086f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7086f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7086f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7086f-126">-ResourceId</span></span>
<span data-ttu-id="7086f-127">ID do recurso da conta de renderização remota.</span><span class="sxs-lookup"><span data-stu-id="7086f-127">Resource ID of Remote Rendering Account.</span></span>

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

### <span data-ttu-id="7086f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7086f-128">-WhatIf</span></span>
<span data-ttu-id="7086f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7086f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7086f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7086f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7086f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7086f-131">CommonParameters</span></span>
<span data-ttu-id="7086f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7086f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7086f-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7086f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7086f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7086f-134">INPUTS</span></span>

### <span data-ttu-id="7086f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7086f-135">System.String</span></span>

### <span data-ttu-id="7086f-136">Microsoft. Azure. Commands. MixedReality. RemoteRenderingAccount. PSRemoteRenderingAccount</span><span class="sxs-lookup"><span data-stu-id="7086f-136">Microsoft.Azure.Commands.MixedReality.RemoteRenderingAccount.PSRemoteRenderingAccount</span></span>

### <span data-ttu-id="7086f-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7086f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7086f-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7086f-138">OUTPUTS</span></span>

### <span data-ttu-id="7086f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7086f-139">System.Boolean</span></span>

## <span data-ttu-id="7086f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7086f-140">NOTES</span></span>

## <span data-ttu-id="7086f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7086f-141">RELATED LINKS</span></span>
