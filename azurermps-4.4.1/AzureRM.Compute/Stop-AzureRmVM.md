---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432240"
---
# <span data-ttu-id="8c763-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="8c763-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c763-102">SYNOPSIS</span></span>
<span data-ttu-id="8c763-103">Interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c763-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c763-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8c763-104">SYNTAX</span></span>

### <span data-ttu-id="8c763-105">ResourceGroupNameParameterSetName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8c763-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c763-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8c763-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c763-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8c763-107">DESCRIPTION</span></span>
<span data-ttu-id="8c763-108">O cmdlet **Stop-AzureRmVM** interrompe uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="8c763-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8c763-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8c763-109">EXAMPLES</span></span>

### <span data-ttu-id="8c763-110">Exemplo 1: parar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="8c763-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8c763-111">Esse comando para a máquina virtual nomeada VirtualMachine07 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8c763-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8c763-112">OS</span><span class="sxs-lookup"><span data-stu-id="8c763-112">PARAMETERS</span></span>

### <span data-ttu-id="8c763-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c763-113">-DefaultProfile</span></span>
<span data-ttu-id="8c763-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8c763-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c763-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8c763-115">-Force</span></span>
<span data-ttu-id="8c763-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8c763-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c763-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8c763-117">-Id</span></span>
<span data-ttu-id="8c763-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c763-118">The resource group name.</span></span>

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

### <span data-ttu-id="8c763-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c763-119">-Name</span></span>
<span data-ttu-id="8c763-120">O nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c763-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="8c763-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c763-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c763-122">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8c763-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8c763-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8c763-123">-StayProvisioned</span></span>
<span data-ttu-id="8c763-124">O cmdlet interrompe todas as máquinas virtuais dentro do VMSS, mas não as desatribui.</span><span class="sxs-lookup"><span data-stu-id="8c763-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="8c763-125">A conta é cobrada pelas máquinas virtuais interrompidas.</span><span class="sxs-lookup"><span data-stu-id="8c763-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="8c763-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8c763-126">-Confirm</span></span>
<span data-ttu-id="8c763-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c763-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c763-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c763-128">-WhatIf</span></span>
<span data-ttu-id="8c763-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8c763-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8c763-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8c763-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c763-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c763-131">CommonParameters</span></span>
<span data-ttu-id="8c763-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c763-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c763-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c763-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c763-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8c763-134">INPUTS</span></span>

## <span data-ttu-id="8c763-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8c763-135">OUTPUTS</span></span>

## <span data-ttu-id="8c763-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8c763-136">NOTES</span></span>

## <span data-ttu-id="8c763-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c763-137">RELATED LINKS</span></span>

[<span data-ttu-id="8c763-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="8c763-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="8c763-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="8c763-141">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="8c763-142">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="8c763-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8c763-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


