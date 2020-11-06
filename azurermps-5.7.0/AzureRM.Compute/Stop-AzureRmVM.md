---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 6cf37c453d47278958ccd84eaf817e6dc118b16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602654"
---
# <span data-ttu-id="8ba33-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="8ba33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ba33-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba33-103">Interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba33-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ba33-104">SYNTAX</span></span>

### <span data-ttu-id="8ba33-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ba33-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba33-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8ba33-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba33-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ba33-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba33-108">O cmdlet **Stop-AzureRmVM** interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba33-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8ba33-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ba33-109">EXAMPLES</span></span>

### <span data-ttu-id="8ba33-110">Exemplo 1: parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8ba33-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8ba33-111">Esse comando para a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8ba33-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8ba33-112">OS</span><span class="sxs-lookup"><span data-stu-id="8ba33-112">PARAMETERS</span></span>

### <span data-ttu-id="8ba33-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ba33-113">-AsJob</span></span>
<span data-ttu-id="8ba33-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8ba33-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8ba33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba33-115">-DefaultProfile</span></span>
<span data-ttu-id="8ba33-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba33-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ba33-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8ba33-117">-Force</span></span>
<span data-ttu-id="8ba33-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8ba33-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8ba33-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8ba33-119">-Id</span></span>
<span data-ttu-id="8ba33-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ba33-120">The resource group name.</span></span>

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

### <span data-ttu-id="8ba33-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ba33-121">-Name</span></span>
<span data-ttu-id="8ba33-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ba33-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba33-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba33-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ba33-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ba33-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8ba33-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8ba33-125">-StayProvisioned</span></span>
<span data-ttu-id="8ba33-126">O cmdlet interrompe todas as máquinas virtuais dentro do VMSS, mas não as desatribui.</span><span class="sxs-lookup"><span data-stu-id="8ba33-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="8ba33-127">A conta é cobrada pelas máquinas virtuais interrompidas.</span><span class="sxs-lookup"><span data-stu-id="8ba33-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="8ba33-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ba33-128">-Confirm</span></span>
<span data-ttu-id="8ba33-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba33-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba33-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba33-130">-WhatIf</span></span>
<span data-ttu-id="8ba33-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ba33-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ba33-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ba33-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba33-133">CommonParameters</span></span>
<span data-ttu-id="8ba33-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba33-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba33-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba33-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ba33-136">INPUTS</span></span>

### <span data-ttu-id="8ba33-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8ba33-137">None</span></span>
<span data-ttu-id="8ba33-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8ba33-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ba33-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ba33-139">OUTPUTS</span></span>

### <span data-ttu-id="8ba33-140">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8ba33-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8ba33-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ba33-141">NOTES</span></span>

## <span data-ttu-id="8ba33-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ba33-142">RELATED LINKS</span></span>

[<span data-ttu-id="8ba33-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8ba33-144">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="8ba33-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="8ba33-146">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="8ba33-147">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="8ba33-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8ba33-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


