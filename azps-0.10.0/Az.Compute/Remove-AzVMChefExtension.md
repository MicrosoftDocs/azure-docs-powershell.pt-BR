---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 595d439707c67363faa7a780f8980efa7a1f3065
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776920"
---
# <span data-ttu-id="91bce-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="91bce-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="91bce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91bce-102">SYNOPSIS</span></span>
<span data-ttu-id="91bce-103">Remove a extensão chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91bce-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="91bce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91bce-104">SYNTAX</span></span>

### <span data-ttu-id="91bce-105">Linux</span><span class="sxs-lookup"><span data-stu-id="91bce-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91bce-106">Windows</span><span class="sxs-lookup"><span data-stu-id="91bce-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91bce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91bce-107">DESCRIPTION</span></span>
<span data-ttu-id="91bce-108">O cmdlet **Remove-AzureVMChefExtension** remove a extensão chefe de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91bce-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="91bce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91bce-109">EXAMPLES</span></span>

### <span data-ttu-id="91bce-110">Exemplo 1: remover uma extensão chefe de um computador virtual do Windows</span><span class="sxs-lookup"><span data-stu-id="91bce-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="91bce-111">Esse comando Remove uma extensão chefe de uma máquina virtual baseada em Windows nomeada WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="91bce-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="91bce-112">Exemplo 2: remover uma extensão chefe de um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="91bce-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="91bce-113">Esse comando Remove uma extensão chefe de uma máquina virtual baseada em Linux nomeada LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="91bce-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="91bce-114">OS</span><span class="sxs-lookup"><span data-stu-id="91bce-114">PARAMETERS</span></span>

### <span data-ttu-id="91bce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bce-115">-DefaultProfile</span></span>
<span data-ttu-id="91bce-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91bce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91bce-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="91bce-117">-Linux</span></span>
<span data-ttu-id="91bce-118">Indica que esse cmdlet destina-se a um computador virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="91bce-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bce-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="91bce-119">-Name</span></span>
<span data-ttu-id="91bce-120">Especifica o nome da extensão chefe que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="91bce-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91bce-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91bce-121">-ResourceGroupName</span></span>
<span data-ttu-id="91bce-122">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="91bce-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="91bce-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="91bce-123">-VMName</span></span>
<span data-ttu-id="91bce-124">Especifica o nome de uma máquina virtual para a qual esse cmdlet Remove a extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="91bce-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="91bce-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="91bce-125">-Windows</span></span>
<span data-ttu-id="91bce-126">Indica que esse cmdlet se destina a um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="91bce-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91bce-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91bce-127">-Confirm</span></span>
<span data-ttu-id="91bce-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91bce-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91bce-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91bce-129">-WhatIf</span></span>
<span data-ttu-id="91bce-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91bce-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="91bce-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91bce-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91bce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bce-132">CommonParameters</span></span>
<span data-ttu-id="91bce-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91bce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bce-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91bce-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bce-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91bce-135">INPUTS</span></span>

### <span data-ttu-id="91bce-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="91bce-136">None</span></span>
<span data-ttu-id="91bce-137">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="91bce-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="91bce-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91bce-138">OUTPUTS</span></span>

### <span data-ttu-id="91bce-139">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="91bce-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="91bce-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91bce-140">NOTES</span></span>

## <span data-ttu-id="91bce-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91bce-141">RELATED LINKS</span></span>

[<span data-ttu-id="91bce-142">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="91bce-142">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="91bce-143">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="91bce-143">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
