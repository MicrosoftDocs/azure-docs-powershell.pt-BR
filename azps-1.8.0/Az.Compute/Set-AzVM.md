---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: a147565a61bc75d71083c69766138c3a5a4659db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771116"
---
# <span data-ttu-id="ff723-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff723-101">Set-AzVM</span></span>

## <span data-ttu-id="ff723-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff723-102">SYNOPSIS</span></span>
<span data-ttu-id="ff723-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ff723-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="ff723-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff723-104">SYNTAX</span></span>

### <span data-ttu-id="ff723-105">GeneralizeResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ff723-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff723-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff723-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff723-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff723-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ff723-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ff723-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff723-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff723-109">DESCRIPTION</span></span>
<span data-ttu-id="ff723-110">O cmdlet **set-AzVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ff723-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="ff723-111">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="ff723-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="ff723-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff723-112">EXAMPLES</span></span>

### <span data-ttu-id="ff723-113">Exemplo 1: marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="ff723-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="ff723-114">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ff723-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="ff723-115">OS</span><span class="sxs-lookup"><span data-stu-id="ff723-115">PARAMETERS</span></span>

### <span data-ttu-id="ff723-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff723-116">-AsJob</span></span>
<span data-ttu-id="ff723-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="ff723-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ff723-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff723-118">-DefaultProfile</span></span>
<span data-ttu-id="ff723-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff723-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff723-120">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="ff723-120">-Generalized</span></span>
<span data-ttu-id="ff723-121">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="ff723-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff723-122">-ID</span><span class="sxs-lookup"><span data-stu-id="ff723-122">-Id</span></span>
<span data-ttu-id="ff723-123">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff723-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff723-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff723-124">-Name</span></span>
<span data-ttu-id="ff723-125">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="ff723-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff723-126">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="ff723-126">-Redeploy</span></span>
<span data-ttu-id="ff723-127">Indica que esse cmdlet reimplanta manualmente a máquina virtual em um host do Azure diferente para corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="ff723-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="ff723-128">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda dos dados da unidade efêmera.</span><span class="sxs-lookup"><span data-stu-id="ff723-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff723-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff723-129">-ResourceGroupName</span></span>
<span data-ttu-id="ff723-130">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff723-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff723-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff723-131">CommonParameters</span></span>
<span data-ttu-id="ff723-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff723-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff723-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff723-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff723-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff723-134">INPUTS</span></span>

### <span data-ttu-id="ff723-135">System. String</span><span class="sxs-lookup"><span data-stu-id="ff723-135">System.String</span></span>

## <span data-ttu-id="ff723-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff723-136">OUTPUTS</span></span>

### <span data-ttu-id="ff723-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ff723-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ff723-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff723-138">NOTES</span></span>

## <span data-ttu-id="ff723-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff723-139">RELATED LINKS</span></span>

[<span data-ttu-id="ff723-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff723-140">Get-AzVM</span></span>](./Get-AzVM.md)


