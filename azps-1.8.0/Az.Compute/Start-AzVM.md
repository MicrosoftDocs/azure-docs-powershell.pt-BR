---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601215"
---
# <span data-ttu-id="1a0e4-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-101">Start-AzVM</span></span>

## <span data-ttu-id="1a0e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1a0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="1a0e4-103">Inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="1a0e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a0e4-104">SYNTAX</span></span>

### <span data-ttu-id="1a0e4-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="1a0e4-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a0e4-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1a0e4-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a0e4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1a0e4-107">DESCRIPTION</span></span>
<span data-ttu-id="1a0e4-108">O cmdlet **Start-AzVM** inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="1a0e4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1a0e4-109">EXAMPLES</span></span>

### <span data-ttu-id="1a0e4-110">Exemplo 1: iniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="1a0e4-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="1a0e4-111">Esse comando inicia a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="1a0e4-112">OS</span><span class="sxs-lookup"><span data-stu-id="1a0e4-112">PARAMETERS</span></span>

### <span data-ttu-id="1a0e4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a0e4-113">-AsJob</span></span>
<span data-ttu-id="1a0e4-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="1a0e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a0e4-115">-DefaultProfile</span></span>
<span data-ttu-id="1a0e4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a0e4-117">-ID</span><span class="sxs-lookup"><span data-stu-id="1a0e4-117">-Id</span></span>
<span data-ttu-id="1a0e4-118">A ID da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-118">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0e4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a0e4-119">-Name</span></span>
<span data-ttu-id="1a0e4-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a0e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a0e4-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a0e4-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1a0e4-123">-Confirm</span></span>
<span data-ttu-id="1a0e4-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a0e4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a0e4-125">-WhatIf</span></span>
<span data-ttu-id="1a0e4-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a0e4-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a0e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a0e4-128">CommonParameters</span></span>
<span data-ttu-id="1a0e4-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a0e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a0e4-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a0e4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a0e4-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1a0e4-131">INPUTS</span></span>

### <span data-ttu-id="1a0e4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1a0e4-132">System.String</span></span>

## <span data-ttu-id="1a0e4-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1a0e4-133">OUTPUTS</span></span>

### <span data-ttu-id="1a0e4-134">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="1a0e4-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="1a0e4-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1a0e4-135">NOTES</span></span>

## <span data-ttu-id="1a0e4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1a0e4-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a0e4-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1a0e4-138">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="1a0e4-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="1a0e4-140">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="1a0e4-141">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="1a0e4-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="1a0e4-142">Update-AzVM</span></span>](./Update-AzVM.md)


