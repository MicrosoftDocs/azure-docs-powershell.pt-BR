---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942116"
---
# <span data-ttu-id="54bc5-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="54bc5-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="54bc5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="54bc5-103">Remove a extensão do AEM de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54bc5-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="54bc5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54bc5-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54bc5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="54bc5-106">O cmdlet **Remove-AzVMAEMExtension** remove a extensão do Azure Enhanced Monitoring (AEM) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54bc5-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="54bc5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="54bc5-108">Exemplo 1: remover a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="54bc5-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="54bc5-109">Esse comando Remove a extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="54bc5-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="54bc5-110">OS</span><span class="sxs-lookup"><span data-stu-id="54bc5-110">PARAMETERS</span></span>

### <span data-ttu-id="54bc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bc5-111">-DefaultProfile</span></span>
<span data-ttu-id="54bc5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54bc5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54bc5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="54bc5-113">-Name</span></span>
<span data-ttu-id="54bc5-114">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="54bc5-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="54bc5-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="54bc5-115">-NoWait</span></span>
<span data-ttu-id="54bc5-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="54bc5-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="54bc5-117">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="54bc5-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="54bc5-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="54bc5-118">-OSType</span></span>
<span data-ttu-id="54bc5-119">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="54bc5-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="54bc5-120">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="54bc5-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="54bc5-121">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="54bc5-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="54bc5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54bc5-122">-ResourceGroupName</span></span>
<span data-ttu-id="54bc5-123">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54bc5-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="54bc5-124">Esse cmdlet Remove a extensão do AEM da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54bc5-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="54bc5-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="54bc5-125">-VMName</span></span>
<span data-ttu-id="54bc5-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="54bc5-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="54bc5-127">Esse cmdlet Remove a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="54bc5-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="54bc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bc5-128">CommonParameters</span></span>
<span data-ttu-id="54bc5-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54bc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bc5-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54bc5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bc5-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54bc5-131">INPUTS</span></span>

### <span data-ttu-id="54bc5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="54bc5-132">System.String</span></span>

## <span data-ttu-id="54bc5-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54bc5-133">OUTPUTS</span></span>

### <span data-ttu-id="54bc5-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="54bc5-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="54bc5-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54bc5-135">NOTES</span></span>

## <span data-ttu-id="54bc5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54bc5-136">RELATED LINKS</span></span>

[<span data-ttu-id="54bc5-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="54bc5-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="54bc5-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="54bc5-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="54bc5-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="54bc5-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


