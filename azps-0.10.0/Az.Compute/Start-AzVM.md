---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775961"
---
# <span data-ttu-id="6de25-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-101">Start-AzVM</span></span>

## <span data-ttu-id="6de25-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6de25-102">SYNOPSIS</span></span>
<span data-ttu-id="6de25-103">Inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6de25-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="6de25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6de25-104">SYNTAX</span></span>

### <span data-ttu-id="6de25-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6de25-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6de25-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6de25-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de25-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6de25-107">DESCRIPTION</span></span>
<span data-ttu-id="6de25-108">O cmdlet **Start-AzVM** inicia uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="6de25-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="6de25-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6de25-109">EXAMPLES</span></span>

### <span data-ttu-id="6de25-110">Exemplo 1: iniciar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="6de25-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6de25-111">Esse comando inicia a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6de25-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="6de25-112">OS</span><span class="sxs-lookup"><span data-stu-id="6de25-112">PARAMETERS</span></span>

### <span data-ttu-id="6de25-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6de25-113">-AsJob</span></span>
<span data-ttu-id="6de25-114">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="6de25-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6de25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de25-115">-DefaultProfile</span></span>
<span data-ttu-id="6de25-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6de25-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6de25-117">-ID</span><span class="sxs-lookup"><span data-stu-id="6de25-117">-Id</span></span>
<span data-ttu-id="6de25-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6de25-118">The resource group name.</span></span>

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

### <span data-ttu-id="6de25-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6de25-119">-Name</span></span>
<span data-ttu-id="6de25-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6de25-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="6de25-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de25-121">-ResourceGroupName</span></span>
<span data-ttu-id="6de25-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6de25-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6de25-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6de25-123">-Confirm</span></span>
<span data-ttu-id="6de25-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6de25-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de25-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de25-125">-WhatIf</span></span>
<span data-ttu-id="6de25-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6de25-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6de25-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6de25-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de25-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de25-128">CommonParameters</span></span>
<span data-ttu-id="6de25-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6de25-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de25-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6de25-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de25-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6de25-131">INPUTS</span></span>

### <span data-ttu-id="6de25-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6de25-132">None</span></span>
<span data-ttu-id="6de25-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6de25-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6de25-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6de25-134">OUTPUTS</span></span>

### <span data-ttu-id="6de25-135">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="6de25-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="6de25-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6de25-136">NOTES</span></span>

## <span data-ttu-id="6de25-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6de25-137">RELATED LINKS</span></span>

[<span data-ttu-id="6de25-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6de25-139">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="6de25-140">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="6de25-141">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="6de25-142">Parar-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="6de25-143">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="6de25-143">Update-AzVM</span></span>](./Update-AzVM.md)


