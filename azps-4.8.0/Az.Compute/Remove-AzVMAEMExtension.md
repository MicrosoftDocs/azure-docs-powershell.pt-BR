---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAEMExtension.md
ms.openlocfilehash: 6ed6176b0f30a754156d2ce03ed0d5acad6e48f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111174"
---
# <span data-ttu-id="de185-101">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de185-101">Remove-AzVMAEMExtension</span></span>

## <span data-ttu-id="de185-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="de185-102">SYNOPSIS</span></span>
<span data-ttu-id="de185-103">Remove a extensão do AEM de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de185-103">Removes the AEM extension from a virtual machine.</span></span>

## <span data-ttu-id="de185-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de185-104">SYNTAX</span></span>

```
Remove-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de185-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="de185-105">DESCRIPTION</span></span>
<span data-ttu-id="de185-106">O cmdlet **Remove-AzVMAEMExtension** remove a extensão do Azure Enhanced Monitoring (AEM) de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de185-106">The **Remove-AzVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="de185-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de185-107">EXAMPLES</span></span>

### <span data-ttu-id="de185-108">Exemplo 1: remover a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="de185-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="de185-109">Esse comando Remove a extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="de185-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="de185-110">OS</span><span class="sxs-lookup"><span data-stu-id="de185-110">PARAMETERS</span></span>

### <span data-ttu-id="de185-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de185-111">-DefaultProfile</span></span>
<span data-ttu-id="de185-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de185-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de185-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="de185-113">-Name</span></span>
<span data-ttu-id="de185-114">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="de185-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="de185-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="de185-115">-NoWait</span></span>
<span data-ttu-id="de185-116">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="de185-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="de185-117">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="de185-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="de185-118">-OSType</span><span class="sxs-lookup"><span data-stu-id="de185-118">-OSType</span></span>
<span data-ttu-id="de185-119">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="de185-119">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="de185-120">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de185-120">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="de185-121">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="de185-121">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="de185-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de185-122">-ResourceGroupName</span></span>
<span data-ttu-id="de185-123">Especifica o nome do grupo de recursos de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de185-123">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="de185-124">Esse cmdlet Remove a extensão do AEM da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de185-124">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="de185-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="de185-125">-VMName</span></span>
<span data-ttu-id="de185-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="de185-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="de185-127">Esse cmdlet Remove a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="de185-127">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="de185-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de185-128">CommonParameters</span></span>
<span data-ttu-id="de185-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de185-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de185-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de185-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de185-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="de185-131">INPUTS</span></span>

### <span data-ttu-id="de185-132">System. String</span><span class="sxs-lookup"><span data-stu-id="de185-132">System.String</span></span>

## <span data-ttu-id="de185-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="de185-133">OUTPUTS</span></span>

### <span data-ttu-id="de185-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="de185-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="de185-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="de185-135">NOTES</span></span>

## <span data-ttu-id="de185-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de185-136">RELATED LINKS</span></span>

[<span data-ttu-id="de185-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de185-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="de185-138">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de185-138">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="de185-139">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="de185-139">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


