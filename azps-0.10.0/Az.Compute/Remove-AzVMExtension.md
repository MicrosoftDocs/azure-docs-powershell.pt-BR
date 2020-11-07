---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: e1b400f2fe3ff973c586fbde9f4003732ad8c6cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776905"
---
# <span data-ttu-id="e99a4-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e99a4-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="e99a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e99a4-102">SYNOPSIS</span></span>
<span data-ttu-id="e99a4-103">Remove uma extensão de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e99a4-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="e99a4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e99a4-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e99a4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e99a4-105">DESCRIPTION</span></span>
<span data-ttu-id="e99a4-106">O cmdlet **Remove-AzVMExtension** remove uma extensão das extensões de máquina virtual de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e99a4-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="e99a4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e99a4-107">EXAMPLES</span></span>

### <span data-ttu-id="e99a4-108">Exemplo 1: remover uma extensão de uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="e99a4-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="e99a4-109">Esse comando Remove a extensão chamada ContosoTest da máquina virtual nomeada VirtualMachine22 em ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e99a4-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="e99a4-110">OS</span><span class="sxs-lookup"><span data-stu-id="e99a4-110">PARAMETERS</span></span>

### <span data-ttu-id="e99a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99a4-111">-DefaultProfile</span></span>
<span data-ttu-id="e99a4-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e99a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e99a4-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e99a4-113">-Force</span></span>
<span data-ttu-id="e99a4-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e99a4-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e99a4-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e99a4-115">-Name</span></span>
<span data-ttu-id="e99a4-116">Especifica o nome da extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e99a4-116">Specifies the name of the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e99a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e99a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="e99a4-118">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e99a4-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e99a4-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="e99a4-119">-VMName</span></span>
<span data-ttu-id="e99a4-120">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão.</span><span class="sxs-lookup"><span data-stu-id="e99a4-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e99a4-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e99a4-121">-Confirm</span></span>
<span data-ttu-id="e99a4-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e99a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e99a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e99a4-123">-WhatIf</span></span>
<span data-ttu-id="e99a4-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e99a4-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e99a4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e99a4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e99a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99a4-126">CommonParameters</span></span>
<span data-ttu-id="e99a4-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99a4-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e99a4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99a4-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e99a4-129">INPUTS</span></span>

### <span data-ttu-id="e99a4-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e99a4-130">None</span></span>
<span data-ttu-id="e99a4-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="e99a4-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e99a4-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e99a4-132">OUTPUTS</span></span>

### <span data-ttu-id="e99a4-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e99a4-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e99a4-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e99a4-134">NOTES</span></span>

## <span data-ttu-id="e99a4-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e99a4-135">RELATED LINKS</span></span>

[<span data-ttu-id="e99a4-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e99a4-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="e99a4-137">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e99a4-137">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


