---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117849"
---
# <span data-ttu-id="3b59a-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3b59a-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="3b59a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b59a-102">SYNOPSIS</span></span>
<span data-ttu-id="3b59a-103">Remove um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3b59a-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="3b59a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b59a-104">SYNTAX</span></span>

### <span data-ttu-id="3b59a-105">DefaultParameter (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3b59a-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b59a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3b59a-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b59a-107">Objectparameter</span><span class="sxs-lookup"><span data-stu-id="3b59a-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b59a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b59a-108">DESCRIPTION</span></span>
<span data-ttu-id="3b59a-109">Remove um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3b59a-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="3b59a-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3b59a-110">EXAMPLES</span></span>

### <span data-ttu-id="3b59a-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3b59a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="3b59a-112">Excluir conjunto de criptografia de disco 'enc1' em 'rg1'</span><span class="sxs-lookup"><span data-stu-id="3b59a-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="3b59a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b59a-113">PARAMETERS</span></span>

### <span data-ttu-id="3b59a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b59a-114">-AsJob</span></span>
<span data-ttu-id="3b59a-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3b59a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3b59a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b59a-116">-DefaultProfile</span></span>
<span data-ttu-id="3b59a-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b59a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b59a-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="3b59a-118">-Force</span></span>
<span data-ttu-id="3b59a-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b59a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b59a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b59a-120">-InputObject</span></span>
<span data-ttu-id="3b59a-121">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3b59a-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="3b59a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b59a-122">-Name</span></span>
<span data-ttu-id="3b59a-123">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="3b59a-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="3b59a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b59a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3b59a-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b59a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3b59a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b59a-126">-ResourceId</span></span>
<span data-ttu-id="3b59a-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="3b59a-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="3b59a-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3b59a-128">-Confirm</span></span>
<span data-ttu-id="3b59a-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b59a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b59a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b59a-130">-WhatIf</span></span>
<span data-ttu-id="3b59a-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3b59a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b59a-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b59a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b59a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b59a-133">CommonParameters</span></span>
<span data-ttu-id="3b59a-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b59a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b59a-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b59a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b59a-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="3b59a-136">INPUTS</span></span>

### <span data-ttu-id="3b59a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3b59a-137">System.String</span></span>

### <span data-ttu-id="3b59a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3b59a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="3b59a-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="3b59a-139">OUTPUTS</span></span>

### <span data-ttu-id="3b59a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="3b59a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="3b59a-141">Notas</span><span class="sxs-lookup"><span data-stu-id="3b59a-141">NOTES</span></span>

## <span data-ttu-id="3b59a-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b59a-142">RELATED LINKS</span></span>
