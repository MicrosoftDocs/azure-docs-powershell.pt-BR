---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4ffb65d4eca9511e179d33c53cb8f515c28aab58
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117904"
---
# <span data-ttu-id="c6645-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="c6645-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="c6645-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6645-102">SYNOPSIS</span></span>
<span data-ttu-id="c6645-103">Atualiza as instâncias de função no domínio de atualização especificado.</span><span class="sxs-lookup"><span data-stu-id="c6645-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="c6645-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6645-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c6645-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6645-105">DESCRIPTION</span></span>
<span data-ttu-id="c6645-106">Atualiza as instâncias de função no domínio de atualização especificado.</span><span class="sxs-lookup"><span data-stu-id="c6645-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="c6645-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c6645-107">EXAMPLES</span></span>

### <span data-ttu-id="c6645-108">Exemplo 1: Atualizar instância de função no domínio de atualização</span><span class="sxs-lookup"><span data-stu-id="c6645-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="c6645-109">Este comando atualiza as instâncias de função na atualização do domínio 0 do serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="c6645-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="c6645-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6645-110">PARAMETERS</span></span>

### <span data-ttu-id="c6645-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6645-111">-AsJob</span></span>
<span data-ttu-id="c6645-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="c6645-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c6645-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c6645-113">-CloudServiceName</span></span>
<span data-ttu-id="c6645-114">Nome do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="c6645-114">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6645-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6645-115">-DefaultProfile</span></span>
<span data-ttu-id="c6645-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6645-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6645-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c6645-117">-NoWait</span></span>
<span data-ttu-id="c6645-118">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="c6645-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c6645-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6645-119">-PassThru</span></span>
<span data-ttu-id="c6645-120">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="c6645-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c6645-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6645-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6645-122">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6645-122">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6645-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6645-123">-SubscriptionId</span></span>
<span data-ttu-id="c6645-124">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c6645-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6645-125">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="c6645-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6645-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="c6645-126">-UpdateDomain</span></span>
<span data-ttu-id="c6645-127">Especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="c6645-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="c6645-128">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c6645-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6645-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c6645-129">-Confirm</span></span>
<span data-ttu-id="c6645-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6645-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6645-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6645-131">-WhatIf</span></span>
<span data-ttu-id="c6645-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c6645-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6645-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6645-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6645-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6645-134">CommonParameters</span></span>
<span data-ttu-id="c6645-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6645-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6645-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6645-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6645-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="c6645-137">INPUTS</span></span>

## <span data-ttu-id="c6645-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="c6645-138">OUTPUTS</span></span>

### <span data-ttu-id="c6645-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6645-139">System.Boolean</span></span>

## <span data-ttu-id="c6645-140">Notas</span><span class="sxs-lookup"><span data-stu-id="c6645-140">NOTES</span></span>

<span data-ttu-id="c6645-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="c6645-141">ALIASES</span></span>

## <span data-ttu-id="c6645-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6645-142">RELATED LINKS</span></span>

