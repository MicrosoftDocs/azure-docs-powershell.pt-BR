---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: ffc22a8937e56537de167046f661ee4b5d262fed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426687"
---
# <span data-ttu-id="a4b9c-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a4b9c-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="a4b9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a4b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b9c-103">Verifica a configuração da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="a4b9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4b9c-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a4b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b9c-106">O cmdlet **Test-AzVMAEMExtension** verifica a configuração da extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="a4b9c-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="a4b9c-107">A extensão do AEM coleta os dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="a4b9c-108">Este cmdlet verifica se os dados de desempenho estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="a4b9c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a4b9c-109">EXAMPLES</span></span>

### <span data-ttu-id="a4b9c-110">Exemplo 1: verificar a configuração da extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="a4b9c-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="a4b9c-111">Esse comando verifica a configuração da extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="a4b9c-112">OS</span><span class="sxs-lookup"><span data-stu-id="a4b9c-112">PARAMETERS</span></span>

### <span data-ttu-id="a4b9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b9c-113">-DefaultProfile</span></span>
<span data-ttu-id="a4b9c-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4b9c-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="a4b9c-115">-OSType</span></span>
<span data-ttu-id="a4b9c-116">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="a4b9c-117">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="a4b9c-118">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="a4b9c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b9c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a4b9c-120">Especifica o nome do grupo de recursos da máquina virtual que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="a4b9c-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="a4b9c-121">-SkipStorageCheck</span></span>
<span data-ttu-id="a4b9c-122">Indica que esse cmdlet ignora a verificação de configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="a4b9c-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="a4b9c-123">-VMName</span></span>
<span data-ttu-id="a4b9c-124">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a4b9c-125">Esse cmdlet testa a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a4b9c-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="a4b9c-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="a4b9c-127">Especifica um período de tempo limite, em minutos, para a verificação da configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="a4b9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b9c-128">CommonParameters</span></span>
<span data-ttu-id="a4b9c-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b9c-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4b9c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b9c-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a4b9c-131">INPUTS</span></span>

### <span data-ttu-id="a4b9c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b9c-132">System.String</span></span>

## <span data-ttu-id="a4b9c-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a4b9c-133">OUTPUTS</span></span>

### <span data-ttu-id="a4b9c-134">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="a4b9c-134">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="a4b9c-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a4b9c-135">NOTES</span></span>

## <span data-ttu-id="a4b9c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a4b9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="a4b9c-137">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a4b9c-137">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="a4b9c-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a4b9c-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="a4b9c-139">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a4b9c-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


