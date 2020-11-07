---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775954"
---
# <span data-ttu-id="8b3c0-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-101">Stop-AzVM</span></span>

## <span data-ttu-id="8b3c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="8b3c0-103">Interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8b3c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b3c0-104">SYNTAX</span></span>

### <span data-ttu-id="8b3c0-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b3c0-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b3c0-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8b3c0-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b3c0-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b3c0-107">DESCRIPTION</span></span>
<span data-ttu-id="8b3c0-108">O cmdlet **Stop-AzVM** interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8b3c0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b3c0-109">EXAMPLES</span></span>

### <span data-ttu-id="8b3c0-110">Exemplo 1: parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8b3c0-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8b3c0-111">Esse comando para a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8b3c0-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b3c0-112">PARAMETERS</span></span>

### <span data-ttu-id="8b3c0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b3c0-113">-AsJob</span></span>
<span data-ttu-id="8b3c0-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8b3c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b3c0-115">-DefaultProfile</span></span>
<span data-ttu-id="8b3c0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b3c0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8b3c0-117">-Force</span></span>
<span data-ttu-id="8b3c0-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b3c0-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8b3c0-119">-Id</span></span>
<span data-ttu-id="8b3c0-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-120">The resource group name.</span></span>

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

### <span data-ttu-id="8b3c0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b3c0-121">-Name</span></span>
<span data-ttu-id="8b3c0-122">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="8b3c0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b3c0-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b3c0-124">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8b3c0-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8b3c0-125">-StayProvisioned</span></span>
<span data-ttu-id="8b3c0-126">O cmdlet interrompe todas as máquinas virtuais dentro do VMSS, mas não as desatribui.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="8b3c0-127">A conta é cobrada pelas máquinas virtuais interrompidas.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="8b3c0-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8b3c0-128">-Confirm</span></span>
<span data-ttu-id="8b3c0-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b3c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b3c0-130">-WhatIf</span></span>
<span data-ttu-id="8b3c0-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b3c0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b3c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b3c0-133">CommonParameters</span></span>
<span data-ttu-id="8b3c0-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b3c0-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b3c0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b3c0-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b3c0-136">INPUTS</span></span>

### <span data-ttu-id="8b3c0-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8b3c0-137">None</span></span>
<span data-ttu-id="8b3c0-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8b3c0-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8b3c0-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b3c0-139">OUTPUTS</span></span>

### <span data-ttu-id="8b3c0-140">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8b3c0-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8b3c0-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b3c0-141">NOTES</span></span>

## <span data-ttu-id="8b3c0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b3c0-142">RELATED LINKS</span></span>

[<span data-ttu-id="8b3c0-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8b3c0-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8b3c0-145">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8b3c0-146">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8b3c0-147">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8b3c0-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8b3c0-148">Update-AzVM</span></span>](./Update-AzVM.md)


