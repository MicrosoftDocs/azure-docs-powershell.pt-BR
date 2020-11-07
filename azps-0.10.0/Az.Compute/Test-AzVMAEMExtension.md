---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/test-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Test-AzVMAEMExtension.md
ms.openlocfilehash: 36fd9813523a5977c1981e6de54384cf71de7dc5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775948"
---
# <span data-ttu-id="4e554-101">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4e554-101">Test-AzVMAEMExtension</span></span>

## <span data-ttu-id="4e554-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e554-102">SYNOPSIS</span></span>
<span data-ttu-id="4e554-103">Verifica a configuração da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="4e554-103">Checks the configuration of the AEM extension.</span></span>

## <span data-ttu-id="4e554-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e554-104">SYNTAX</span></span>

```
Test-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e554-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e554-105">DESCRIPTION</span></span>
<span data-ttu-id="4e554-106">O cmdlet **Test-AzVMAEMExtension** verifica a configuração da extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="4e554-106">The **Test-AzVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="4e554-107">A extensão do AEM coleta os dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="4e554-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="4e554-108">Este cmdlet verifica se os dados de desempenho estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="4e554-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="4e554-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e554-109">EXAMPLES</span></span>

### <span data-ttu-id="4e554-110">Exemplo 1: verificar a configuração da extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="4e554-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="4e554-111">Esse comando verifica a configuração da extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="4e554-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="4e554-112">OS</span><span class="sxs-lookup"><span data-stu-id="4e554-112">PARAMETERS</span></span>

### <span data-ttu-id="4e554-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e554-113">-DefaultProfile</span></span>
<span data-ttu-id="4e554-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e554-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e554-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="4e554-115">-OSType</span></span>
<span data-ttu-id="4e554-116">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4e554-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="4e554-117">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4e554-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="4e554-118">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="4e554-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e554-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e554-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e554-120">Especifica o nome do grupo de recursos da máquina virtual que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="4e554-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="4e554-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="4e554-121">-SkipStorageCheck</span></span>
<span data-ttu-id="4e554-122">Indica que esse cmdlet ignora a verificação de configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4e554-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e554-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="4e554-123">-VMName</span></span>
<span data-ttu-id="4e554-124">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="4e554-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="4e554-125">Esse cmdlet testa a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4e554-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="4e554-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="4e554-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="4e554-127">Especifica um período de tempo limite, em minutos, para a verificação da configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4e554-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e554-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e554-128">CommonParameters</span></span>
<span data-ttu-id="4e554-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e554-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e554-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e554-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e554-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e554-131">INPUTS</span></span>

### <span data-ttu-id="4e554-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4e554-132">None</span></span>
<span data-ttu-id="4e554-133">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="4e554-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e554-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e554-134">OUTPUTS</span></span>

### <span data-ttu-id="4e554-135">Microsoft. Azure. Commands. COMPUTE. Extension. AEM. AEMTestResult</span><span class="sxs-lookup"><span data-stu-id="4e554-135">Microsoft.Azure.Commands.Compute.Extension.AEM.AEMTestResult</span></span>

## <span data-ttu-id="4e554-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e554-136">NOTES</span></span>

## <span data-ttu-id="4e554-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e554-137">RELATED LINKS</span></span>

[<span data-ttu-id="4e554-138">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4e554-138">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="4e554-139">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4e554-139">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="4e554-140">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="4e554-140">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)


