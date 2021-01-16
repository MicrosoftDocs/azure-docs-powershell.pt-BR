---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskEncryptionSet.md
ms.openlocfilehash: a15dd51bad097aafcc517fbef67f89d65b076380
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263625"
---
# <span data-ttu-id="1c86b-101">Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1c86b-101">Remove-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="1c86b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1c86b-102">SYNOPSIS</span></span>
<span data-ttu-id="1c86b-103">Remove um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="1c86b-103">Removes a disk encryption set.</span></span>

## <span data-ttu-id="1c86b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c86b-104">SYNTAX</span></span>

### <span data-ttu-id="1c86b-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="1c86b-105">DefaultParameter (Default)</span></span>
```
Remove-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c86b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1c86b-106">ResourceIdParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c86b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1c86b-107">ObjectParameter</span></span>
```
Remove-AzDiskEncryptionSet [-Force] [-InputObject] <PSDiskEncryptionSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c86b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1c86b-108">DESCRIPTION</span></span>
<span data-ttu-id="1c86b-109">Remove um conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="1c86b-109">Removes a disk encryption set.</span></span>

## <span data-ttu-id="1c86b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c86b-110">EXAMPLES</span></span>

### <span data-ttu-id="1c86b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c86b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -Force;
```

<span data-ttu-id="1c86b-112">Excluir o conjunto de criptografia de disco ' enc1 ' em ' Rg1 '</span><span class="sxs-lookup"><span data-stu-id="1c86b-112">Delete disk encryption set 'enc1' in 'rg1'</span></span>

## <span data-ttu-id="1c86b-113">OS</span><span class="sxs-lookup"><span data-stu-id="1c86b-113">PARAMETERS</span></span>

### <span data-ttu-id="1c86b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c86b-114">-AsJob</span></span>
<span data-ttu-id="1c86b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1c86b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c86b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c86b-116">-DefaultProfile</span></span>
<span data-ttu-id="1c86b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c86b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c86b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1c86b-118">-Force</span></span>
<span data-ttu-id="1c86b-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1c86b-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1c86b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c86b-120">-InputObject</span></span>
<span data-ttu-id="1c86b-121">O objeto local do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="1c86b-121">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="1c86b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c86b-122">-Name</span></span>
<span data-ttu-id="1c86b-123">Nome do conjunto de criptografia de disco.</span><span class="sxs-lookup"><span data-stu-id="1c86b-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="1c86b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c86b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c86b-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1c86b-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c86b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c86b-126">-ResourceId</span></span>
<span data-ttu-id="1c86b-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="1c86b-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="1c86b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1c86b-128">-Confirm</span></span>
<span data-ttu-id="1c86b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c86b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c86b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c86b-130">-WhatIf</span></span>
<span data-ttu-id="1c86b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c86b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c86b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c86b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c86b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c86b-133">CommonParameters</span></span>
<span data-ttu-id="1c86b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c86b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c86b-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c86b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c86b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1c86b-136">INPUTS</span></span>

### <span data-ttu-id="1c86b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1c86b-137">System.String</span></span>

### <span data-ttu-id="1c86b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="1c86b-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="1c86b-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1c86b-139">OUTPUTS</span></span>

### <span data-ttu-id="1c86b-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="1c86b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="1c86b-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1c86b-141">NOTES</span></span>

## <span data-ttu-id="1c86b-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c86b-142">RELATED LINKS</span></span>
