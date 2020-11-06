---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: c2b2b1984a61c70d82ed29e434ab5959acaee632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597321"
---
# <span data-ttu-id="8bcb6-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="8bcb6-101">Remove-AzHost</span></span>

## <span data-ttu-id="8bcb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8bcb6-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcb6-103">Remove um host.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-103">Removes a host.</span></span>

## <span data-ttu-id="8bcb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8bcb6-104">SYNTAX</span></span>

### <span data-ttu-id="8bcb6-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="8bcb6-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bcb6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="8bcb6-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bcb6-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="8bcb6-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bcb6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8bcb6-108">DESCRIPTION</span></span>
<span data-ttu-id="8bcb6-109">Este cmdlet excluirá um host</span><span class="sxs-lookup"><span data-stu-id="8bcb6-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="8bcb6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8bcb6-110">EXAMPLES</span></span>

### <span data-ttu-id="8bcb6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8bcb6-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="8bcb6-112">Esse comando obtém e remove o host fornecido.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="8bcb6-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8bcb6-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="8bcb6-114">Esse comando Remove o host fornecido.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-114">This command removes the given host.</span></span>

## <span data-ttu-id="8bcb6-115">OS</span><span class="sxs-lookup"><span data-stu-id="8bcb6-115">PARAMETERS</span></span>

### <span data-ttu-id="8bcb6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8bcb6-116">-AsJob</span></span>
<span data-ttu-id="8bcb6-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8bcb6-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8bcb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bcb6-118">-DefaultProfile</span></span>
<span data-ttu-id="8bcb6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bcb6-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="8bcb6-120">-HostGroupName</span></span>
<span data-ttu-id="8bcb6-121">O nome do grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bcb6-122">-InputObject</span></span>
<span data-ttu-id="8bcb6-123">O objeto local do host.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8bcb6-124">-Name</span></span>
<span data-ttu-id="8bcb6-125">O nome do host.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bcb6-126">-ResourceGroupName</span></span>
<span data-ttu-id="8bcb6-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bcb6-128">-ResourceId</span></span>
<span data-ttu-id="8bcb6-129">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb6-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8bcb6-130">-Confirm</span></span>
<span data-ttu-id="8bcb6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bcb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bcb6-132">-WhatIf</span></span>
<span data-ttu-id="8bcb6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bcb6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bcb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcb6-135">CommonParameters</span></span>
<span data-ttu-id="8bcb6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bcb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcb6-137">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bcb6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcb6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8bcb6-138">INPUTS</span></span>

### <span data-ttu-id="8bcb6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8bcb6-139">System.String</span></span>

### <span data-ttu-id="8bcb6-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="8bcb6-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="8bcb6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8bcb6-141">OUTPUTS</span></span>

### <span data-ttu-id="8bcb6-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8bcb6-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8bcb6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8bcb6-143">NOTES</span></span>

## <span data-ttu-id="8bcb6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8bcb6-144">RELATED LINKS</span></span>
