---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f816be5d3c024e43074d6a75c5ba79df4b2fdb3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785548"
---
# <span data-ttu-id="302a2-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="302a2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="302a2-102">SYNOPSIS</span></span>
<span data-ttu-id="302a2-103">Remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="302a2-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="302a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="302a2-104">SYNTAX</span></span>

### <span data-ttu-id="302a2-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="302a2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="302a2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="302a2-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="302a2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="302a2-107">DESCRIPTION</span></span>
<span data-ttu-id="302a2-108">O cmdlet **Remove-AzureRmVM** remove uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="302a2-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="302a2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="302a2-109">EXAMPLES</span></span>

### <span data-ttu-id="302a2-110">Exemplo 1: remover uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="302a2-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="302a2-111">Esse comando Remove a máquina virtual nomeada VirtualMachine07 na ResourceGroup11 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="302a2-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="302a2-112">OS</span><span class="sxs-lookup"><span data-stu-id="302a2-112">PARAMETERS</span></span>

### <span data-ttu-id="302a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="302a2-113">-AsJob</span></span>
<span data-ttu-id="302a2-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="302a2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="302a2-115">-DefaultProfile</span></span>
<span data-ttu-id="302a2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="302a2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="302a2-117">-Force</span></span>
<span data-ttu-id="302a2-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="302a2-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="302a2-119">-Id</span></span>
<span data-ttu-id="302a2-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="302a2-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="302a2-121">-Name</span></span>
<span data-ttu-id="302a2-122">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="302a2-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="302a2-123">-ResourceGroupName</span></span>
<span data-ttu-id="302a2-124">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="302a2-124">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="302a2-125">-Confirm</span></span>
<span data-ttu-id="302a2-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="302a2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="302a2-127">-WhatIf</span></span>
<span data-ttu-id="302a2-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="302a2-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="302a2-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="302a2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="302a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="302a2-130">CommonParameters</span></span>
<span data-ttu-id="302a2-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="302a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="302a2-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="302a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="302a2-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="302a2-133">INPUTS</span></span>

### <span data-ttu-id="302a2-134">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="302a2-134">None</span></span>
<span data-ttu-id="302a2-135">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="302a2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="302a2-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="302a2-136">OUTPUTS</span></span>

### <span data-ttu-id="302a2-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="302a2-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="302a2-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="302a2-138">NOTES</span></span>

## <span data-ttu-id="302a2-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="302a2-139">RELATED LINKS</span></span>

[<span data-ttu-id="302a2-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="302a2-141">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="302a2-142">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="302a2-143">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="302a2-144">Parar-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="302a2-145">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="302a2-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


