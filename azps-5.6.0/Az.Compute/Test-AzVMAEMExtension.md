---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 040e7e557934fc90e5609a42c2e553ccf34d2f8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892999"
---
# <span data-ttu-id="264c6-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="264c6-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="264c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="264c6-102">SYNOPSIS</span></span>
<span data-ttu-id="264c6-103">Verifica a configuração da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="264c6-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="264c6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="264c6-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="264c6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="264c6-105">DESCRIPTION</span></span>
<span data-ttu-id="264c6-106">O cmdlet **Test-AzVMAEMExtension** verifica a configuração da extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="264c6-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="264c6-107">A extensão do AEM coleta os dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="264c6-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="264c6-108">Este cmdlet verifica se os dados de desempenho estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="264c6-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="264c6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="264c6-109">EXAMPLES</span></span>

### <span data-ttu-id="264c6-110">Exemplo 1: Verificar a configuração da extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="264c6-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="264c6-111">Este comando verifica a configuração da extensão do AEM para a máquina virtual chamada contoso-server.</span><span class="sxs-lookup"><span data-stu-id="264c6-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="264c6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="264c6-112">PARAMETERS</span></span>

### <span data-ttu-id="264c6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264c6-113">-DefaultProfile</span></span>
<span data-ttu-id="264c6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="264c6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="264c6-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="264c6-115">-OSType</span></span>
<span data-ttu-id="264c6-116">Especifica o tipo do sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="264c6-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="264c6-117">Se o disco do sistema operacional não tiver um tipo, especifique esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="264c6-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="264c6-118">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="264c6-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264c6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="264c6-119">-ResourceGroupName</span></span>
<span data-ttu-id="264c6-120">Especifica o nome do grupo de recursos da máquina virtual que esse cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="264c6-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="264c6-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="264c6-121">-SkipStorageCheck</span></span>
<span data-ttu-id="264c6-122">Indica que esse cmdlet ignora a verificação da configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="264c6-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264c6-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="264c6-123">-VMName</span></span>
<span data-ttu-id="264c6-124">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="264c6-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="264c6-125">Este cmdlet testa a extensão do AEM para a máquina virtual especificada por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="264c6-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="264c6-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="264c6-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="264c6-127">Especifica um período de tempo de tempo, em minutos, para a verificação de configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="264c6-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264c6-128">CommonParameters</span></span>
<span data-ttu-id="264c6-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="264c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264c6-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="264c6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264c6-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="264c6-131">INPUTS</span></span>

### <span data-ttu-id="264c6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="264c6-132">System.String</span></span>

## <span data-ttu-id="264c6-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="264c6-133">OUTPUTS</span></span>

### <span data-ttu-id="264c6-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="264c6-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="264c6-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="264c6-135">NOTES</span></span>

## <span data-ttu-id="264c6-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="264c6-136">RELATED LINKS</span></span>

[<span data-ttu-id="264c6-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="264c6-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="264c6-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="264c6-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="264c6-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="264c6-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


