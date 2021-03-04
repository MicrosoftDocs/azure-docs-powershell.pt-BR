---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 71fcf62049cfb15e830b4c8c5f311c042de55bb9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886081"
---
# <span data-ttu-id="9b8be-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b8be-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="9b8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b8be-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8be-103">Remove a extensão do AEM de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b8be-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="9b8be-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9b8be-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b8be-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9b8be-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8be-106">O cmdlet **Remove-AzVMAEMExtension** remove a extensão do Azure Enhanced Monitoring (AEM) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b8be-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="9b8be-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b8be-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8be-108">Exemplo 1: Remover a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="9b8be-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="9b8be-109">Este comando remove a extensão do AEM para a máquina virtual chamada contoso-server.</span><span class="sxs-lookup"><span data-stu-id="9b8be-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="9b8be-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9b8be-110">PARAMETERS</span></span>

### <span data-ttu-id="9b8be-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8be-111">-DefaultProfile</span></span>
<span data-ttu-id="9b8be-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9b8be-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b8be-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9b8be-113">-Name</span></span>
<span data-ttu-id="9b8be-114">Especifica o nome da máquina virtual da qual este cmdlet remove a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="9b8be-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8be-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9b8be-115">-NoWait</span></span>
<span data-ttu-id="9b8be-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="9b8be-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9b8be-117">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="9b8be-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9b8be-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="9b8be-118">-OSType</span></span>
<span data-ttu-id="9b8be-119">Especifica o tipo do sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9b8be-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="9b8be-120">Se o disco do sistema operacional não tiver um tipo, especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9b8be-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="9b8be-121">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="9b8be-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b8be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8be-122">-ResourceGroupName</span></span>
<span data-ttu-id="9b8be-123">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b8be-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="9b8be-124">Este cmdlet remove a extensão do AEM dessa máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b8be-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8be-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="9b8be-125">-VMName</span></span>
<span data-ttu-id="9b8be-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9b8be-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9b8be-127">Este cmdlet remove a extensão do AEM para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9b8be-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8be-128">CommonParameters</span></span>
<span data-ttu-id="9b8be-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8be-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b8be-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8be-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b8be-131">INPUTS</span></span>

### <span data-ttu-id="9b8be-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9b8be-132">System.String</span></span>

## <span data-ttu-id="9b8be-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9b8be-133">OUTPUTS</span></span>

### <span data-ttu-id="9b8be-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9b8be-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9b8be-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="9b8be-135">NOTES</span></span>

## <span data-ttu-id="9b8be-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b8be-136">RELATED LINKS</span></span>

[<span data-ttu-id="9b8be-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b8be-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="9b8be-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b8be-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="9b8be-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9b8be-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


