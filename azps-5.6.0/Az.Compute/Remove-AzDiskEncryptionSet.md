---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: ec146441e620580b5028dffa4e0f7f3e09c45b35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890003"
---
# <span data-ttu-id="0568b-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0568b-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="0568b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0568b-102">SYNOPSIS</span></span>
<span data-ttu-id="0568b-103">Remove um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="0568b-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="0568b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0568b-104">SYNTAX</span></span>

### <span data-ttu-id="0568b-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0568b-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0568b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="0568b-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0568b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="0568b-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0568b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0568b-108">DESCRIPTION</span></span>
<span data-ttu-id="0568b-109">Remove um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="0568b-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="0568b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0568b-110">EXAMPLES</span></span>

### <span data-ttu-id="0568b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0568b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="0568b-112">Excluir conjunto de criptografia de disco 'enc1' em 'rg1'</span><span class="sxs-lookup"><span data-stu-id="0568b-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="0568b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0568b-113">PARAMETERS</span></span>

### <span data-ttu-id="0568b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0568b-114">-AsJob</span></span>
<span data-ttu-id="0568b-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0568b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0568b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0568b-116">-DefaultProfile</span></span>
<span data-ttu-id="0568b-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0568b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0568b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0568b-118">-Force</span></span>
<span data-ttu-id="0568b-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="0568b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0568b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0568b-120">-InputObject</span></span>
<span data-ttu-id="0568b-121">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="0568b-121">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0568b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0568b-122">-Name</span></span>
<span data-ttu-id="0568b-123">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="0568b-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0568b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0568b-124">-ResourceGroupName</span></span>
<span data-ttu-id="0568b-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0568b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0568b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0568b-126">-ResourceId</span></span>
<span data-ttu-id="0568b-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="0568b-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="0568b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0568b-128">-Confirm</span></span>
<span data-ttu-id="0568b-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0568b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0568b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0568b-130">-WhatIf</span></span>
<span data-ttu-id="0568b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0568b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0568b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0568b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0568b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0568b-133">CommonParameters</span></span>
<span data-ttu-id="0568b-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0568b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0568b-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0568b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0568b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0568b-136">INPUTS</span></span>

### <span data-ttu-id="0568b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0568b-137">System.String</span></span>

### <span data-ttu-id="0568b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0568b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="0568b-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0568b-139">OUTPUTS</span></span>

### <span data-ttu-id="0568b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="0568b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="0568b-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="0568b-141">NOTES</span></span>

## <span data-ttu-id="0568b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0568b-142">RELATED LINKS</span></span>
