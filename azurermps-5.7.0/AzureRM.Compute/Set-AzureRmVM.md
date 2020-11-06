---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: d17d01295d118c3927c127a367747cfde428ccfd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426782"
---
# <span data-ttu-id="a70f5-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a70f5-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="a70f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a70f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a70f5-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="a70f5-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a70f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a70f5-104">SYNTAX</span></span>

### <span data-ttu-id="a70f5-105">GeneralizeResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a70f5-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a70f5-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a70f5-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a70f5-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a70f5-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a70f5-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a70f5-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a70f5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a70f5-109">DESCRIPTION</span></span>
<span data-ttu-id="a70f5-110">O cmdlet **set-AzureRmVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="a70f5-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="a70f5-111">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="a70f5-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="a70f5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a70f5-112">EXAMPLES</span></span>

### <span data-ttu-id="a70f5-113">Exemplo 1: marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="a70f5-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="a70f5-114">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="a70f5-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="a70f5-115">OS</span><span class="sxs-lookup"><span data-stu-id="a70f5-115">PARAMETERS</span></span>

### <span data-ttu-id="a70f5-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a70f5-116">-AsJob</span></span>
<span data-ttu-id="a70f5-117">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a70f5-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a70f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70f5-118">-DefaultProfile</span></span>
<span data-ttu-id="a70f5-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a70f5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a70f5-120">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="a70f5-120">-Generalized</span></span>
<span data-ttu-id="a70f5-121">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="a70f5-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70f5-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a70f5-122">-Id</span></span>
<span data-ttu-id="a70f5-123">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a70f5-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70f5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="a70f5-124">-Name</span></span>
<span data-ttu-id="a70f5-125">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="a70f5-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="a70f5-126">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="a70f5-126">-Redeploy</span></span>
<span data-ttu-id="a70f5-127">Indica que esse cmdlet reimplanta manualmente a máquina virtual em um host do Azure diferente para corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="a70f5-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="a70f5-128">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda dos dados da unidade efêmera.</span><span class="sxs-lookup"><span data-stu-id="a70f5-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70f5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70f5-129">-ResourceGroupName</span></span>
<span data-ttu-id="a70f5-130">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a70f5-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70f5-131">CommonParameters</span></span>
<span data-ttu-id="a70f5-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70f5-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a70f5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70f5-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a70f5-134">INPUTS</span></span>

### <span data-ttu-id="a70f5-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a70f5-135">None</span></span>
<span data-ttu-id="a70f5-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a70f5-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a70f5-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a70f5-137">OUTPUTS</span></span>

### <span data-ttu-id="a70f5-138">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a70f5-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="a70f5-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a70f5-139">NOTES</span></span>

## <span data-ttu-id="a70f5-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a70f5-140">RELATED LINKS</span></span>

[<span data-ttu-id="a70f5-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a70f5-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


