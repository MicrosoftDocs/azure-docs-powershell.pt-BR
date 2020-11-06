---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3c6f1ca4a50ccc359c1bbf10e63c9a9c0baf05fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441150"
---
# <span data-ttu-id="0c903-101">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0c903-101">Test-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="0c903-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c903-102">SYNOPSIS</span></span>
<span data-ttu-id="0c903-103">Verifica a configuração da extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="0c903-103">Checks the configuration of the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c903-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c903-104">SYNTAX</span></span>

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c903-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0c903-105">DESCRIPTION</span></span>
<span data-ttu-id="0c903-106">O cmdlet **Test-AzureRmVMAEMExtension** verifica a configuração da extensão do Azure Enhanced Monitoring (AEM).</span><span class="sxs-lookup"><span data-stu-id="0c903-106">The **Test-AzureRmVMAEMExtension** cmdlet checks the configuration of the Azure Enhanced Monitoring (AEM) extension.</span></span>
<span data-ttu-id="0c903-107">A extensão do AEM coleta os dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="0c903-107">The AEM extension collects the performance data.</span></span>
<span data-ttu-id="0c903-108">Este cmdlet verifica se os dados de desempenho estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0c903-108">This cmdlet checks whether performance data is available.</span></span>

## <span data-ttu-id="0c903-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c903-109">EXAMPLES</span></span>

### <span data-ttu-id="0c903-110">Exemplo 1: verificar a configuração da extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="0c903-110">Example 1: Check the configuration of the AEM extension</span></span>
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="0c903-111">Esse comando verifica a configuração da extensão do AEM para a máquina virtual nomeada contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="0c903-111">This command checks the configuration of the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="0c903-112">OS</span><span class="sxs-lookup"><span data-stu-id="0c903-112">PARAMETERS</span></span>

### <span data-ttu-id="0c903-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c903-113">-DefaultProfile</span></span>
<span data-ttu-id="0c903-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c903-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c903-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="0c903-115">-OSType</span></span>
<span data-ttu-id="0c903-116">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="0c903-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="0c903-117">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0c903-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="0c903-118">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="0c903-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="0c903-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c903-119">-ResourceGroupName</span></span>
<span data-ttu-id="0c903-120">Especifica o nome do grupo de recursos da máquina virtual que este cmdlet verifica.</span><span class="sxs-lookup"><span data-stu-id="0c903-120">Specifies the name of the resource group of the virtual machine that this cmdlet checks.</span></span>

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

### <span data-ttu-id="0c903-121">-SkipStorageCheck</span><span class="sxs-lookup"><span data-stu-id="0c903-121">-SkipStorageCheck</span></span>
<span data-ttu-id="0c903-122">Indica que esse cmdlet ignora a verificação de configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0c903-122">Indicates that this cmdlet skips the check of storage configuration.</span></span>

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

### <span data-ttu-id="0c903-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="0c903-123">-VMName</span></span>
<span data-ttu-id="0c903-124">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0c903-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="0c903-125">Esse cmdlet testa a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0c903-125">This cmdlet tests the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c903-126">-WaitTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="0c903-126">-WaitTimeInMinutes</span></span>
<span data-ttu-id="0c903-127">Especifica um período de tempo limite, em minutos, para a verificação da configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0c903-127">Specifies a time-out period, in minutes, for the storage configuration check.</span></span>

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

### <span data-ttu-id="0c903-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c903-128">CommonParameters</span></span>
<span data-ttu-id="0c903-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c903-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c903-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c903-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c903-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0c903-131">INPUTS</span></span>

## <span data-ttu-id="0c903-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0c903-132">OUTPUTS</span></span>

## <span data-ttu-id="0c903-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0c903-133">NOTES</span></span>

## <span data-ttu-id="0c903-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c903-134">RELATED LINKS</span></span>

[<span data-ttu-id="0c903-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0c903-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="0c903-136">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0c903-136">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="0c903-137">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="0c903-137">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

