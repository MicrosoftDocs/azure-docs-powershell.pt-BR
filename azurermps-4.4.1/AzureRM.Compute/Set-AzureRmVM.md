---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610020"
---
# <span data-ttu-id="d5b44-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d5b44-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="d5b44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5b44-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b44-103">Marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d5b44-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5b44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5b44-104">SYNTAX</span></span>

### <span data-ttu-id="d5b44-105">GeneralizeResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5b44-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5b44-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d5b44-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5b44-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d5b44-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b44-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d5b44-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5b44-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5b44-109">DESCRIPTION</span></span>
<span data-ttu-id="d5b44-110">O cmdlet **set-AzureRmVM** marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d5b44-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="d5b44-111">Antes de executar este cmdlet, faça logon na máquina virtual e use o Sysprep para preparar o disco rígido.</span><span class="sxs-lookup"><span data-stu-id="d5b44-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="d5b44-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5b44-112">EXAMPLES</span></span>

### <span data-ttu-id="d5b44-113">Exemplo 1: marcar uma máquina virtual como generalizada</span><span class="sxs-lookup"><span data-stu-id="d5b44-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="d5b44-114">Esse comando marca a máquina virtual chamada VirtualMachine07 como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d5b44-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="d5b44-115">OS</span><span class="sxs-lookup"><span data-stu-id="d5b44-115">PARAMETERS</span></span>

### <span data-ttu-id="d5b44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b44-116">-DefaultProfile</span></span>
<span data-ttu-id="d5b44-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b44-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b44-118">-Generalizado</span><span class="sxs-lookup"><span data-stu-id="d5b44-118">-Generalized</span></span>
<span data-ttu-id="d5b44-119">Indica que esse cmdlet marca uma máquina virtual como generalizada.</span><span class="sxs-lookup"><span data-stu-id="d5b44-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b44-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d5b44-120">-Id</span></span>
<span data-ttu-id="d5b44-121">Especifica a ID do recurso da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d5b44-121">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="d5b44-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5b44-122">-Name</span></span>
<span data-ttu-id="d5b44-123">Especifica o nome da máquina virtual na qual esse cmdlet funciona.</span><span class="sxs-lookup"><span data-stu-id="d5b44-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b44-124">-Reimplantar</span><span class="sxs-lookup"><span data-stu-id="d5b44-124">-Redeploy</span></span>
<span data-ttu-id="d5b44-125">Indica que esse cmdlet reimplanta manualmente a máquina virtual em um host do Azure diferente para corrigir os problemas.</span><span class="sxs-lookup"><span data-stu-id="d5b44-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="d5b44-126">Se você reimplantar uma máquina virtual, ela será reiniciada, o que resulta na perda dos dados da unidade efêmera.</span><span class="sxs-lookup"><span data-stu-id="d5b44-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b44-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b44-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5b44-128">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d5b44-128">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d5b44-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b44-129">CommonParameters</span></span>
<span data-ttu-id="d5b44-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b44-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b44-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5b44-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b44-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5b44-132">INPUTS</span></span>

## <span data-ttu-id="d5b44-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5b44-133">OUTPUTS</span></span>

## <span data-ttu-id="d5b44-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5b44-134">NOTES</span></span>

## <span data-ttu-id="d5b44-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5b44-135">RELATED LINKS</span></span>

[<span data-ttu-id="d5b44-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="d5b44-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


