---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: 931ed484850654ecebc368ced0b378ce2a40944f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426939"
---
# <span data-ttu-id="b9a83-101">Set-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b9a83-101">Set-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="b9a83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9a83-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a83-103">Habilita o suporte para monitoramento de sistemas SAP.</span><span class="sxs-lookup"><span data-stu-id="b9a83-103">Enables support for monitoring for SAP systems.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9a83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9a83-104">SYNTAX</span></span>

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9a83-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9a83-105">DESCRIPTION</span></span>
<span data-ttu-id="b9a83-106">O cmdlet **set-AzureRmVMAEMExtension** atualiza a configuração de uma máquina virtual para habilitar ou atualizar o suporte para o monitoramento de sistemas SAP instalados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9a83-106">The **Set-AzureRmVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="b9a83-107">O cmdlet instala a extensão do Azure Enhanced Monitoring (AEM) que coleta os dados de desempenho e o torna detectável para o sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="b9a83-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="b9a83-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9a83-108">EXAMPLES</span></span>

### <span data-ttu-id="b9a83-109">Exemplo 1: usar a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="b9a83-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="b9a83-110">Este comando configura a máquina virtual chamada contoso-Server para usar a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="b9a83-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="b9a83-111">O comando especifica a conta de armazenamento chamada stdstorage.</span><span class="sxs-lookup"><span data-stu-id="b9a83-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="b9a83-112">OS</span><span class="sxs-lookup"><span data-stu-id="b9a83-112">PARAMETERS</span></span>

### <span data-ttu-id="b9a83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a83-113">-DefaultProfile</span></span>
<span data-ttu-id="b9a83-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9a83-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9a83-115">-DisableWAD</span><span class="sxs-lookup"><span data-stu-id="b9a83-115">-DisableWAD</span></span>
<span data-ttu-id="b9a83-116">Indica que esse cmdlet não habilita o diagnóstico do Azure para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9a83-116">Indicates that this cmdlet does not enable Azure Diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="b9a83-117">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="b9a83-117">-EnableWAD</span></span>
<span data-ttu-id="b9a83-118">Se esse parâmetro for fornecido, o commandlet habilitará o diagnóstico do Windows Azure para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9a83-118">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9a83-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="b9a83-119">-OSType</span></span>
<span data-ttu-id="b9a83-120">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b9a83-120">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="b9a83-121">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b9a83-121">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="b9a83-122">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="b9a83-122">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="b9a83-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a83-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9a83-124">Especifica o nome do grupo de recursos da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="b9a83-124">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b9a83-125">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="b9a83-125">-SkipStorage</span></span>
<span data-ttu-id="b9a83-126">Indica que esse cmdlet ignora a configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9a83-126">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="b9a83-127">-VMName</span><span class="sxs-lookup"><span data-stu-id="b9a83-127">-VMName</span></span>
<span data-ttu-id="b9a83-128">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b9a83-128">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b9a83-129">Esse cmdlet adiciona a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="b9a83-129">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9a83-130">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b9a83-130">-WADStorageAccountName</span></span>
<span data-ttu-id="b9a83-131">Especifica o nome da conta de armazenamento que este cmdlet usa para configurar a extensão LinuxDiagnostics ou IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="b9a83-131">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="b9a83-132">Se a máquina virtual não usar uma conta de armazenamento padrão, você deve especificar um valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b9a83-132">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="b9a83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a83-133">CommonParameters</span></span>
<span data-ttu-id="b9a83-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9a83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a83-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a83-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a83-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9a83-136">INPUTS</span></span>

## <span data-ttu-id="b9a83-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9a83-137">OUTPUTS</span></span>

## <span data-ttu-id="b9a83-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9a83-138">NOTES</span></span>

## <span data-ttu-id="b9a83-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9a83-139">RELATED LINKS</span></span>

[<span data-ttu-id="b9a83-140">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b9a83-140">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="b9a83-141">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b9a83-141">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="b9a83-142">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="b9a83-142">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


