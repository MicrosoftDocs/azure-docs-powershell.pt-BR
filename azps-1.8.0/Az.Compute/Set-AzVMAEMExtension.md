---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: d79be4ce619d8673a8b3811eb5fa2e0c3602beb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771114"
---
# <span data-ttu-id="9f648-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9f648-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="9f648-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f648-102">SYNOPSIS</span></span>
<span data-ttu-id="9f648-103">Habilita o suporte para monitoramento de sistemas SAP.</span><span class="sxs-lookup"><span data-stu-id="9f648-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="9f648-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f648-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f648-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f648-105">DESCRIPTION</span></span>
<span data-ttu-id="9f648-106">O cmdlet **set-AzVMAEMExtension** atualiza a configuração de uma máquina virtual para habilitar ou atualizar o suporte para o monitoramento de sistemas SAP instalados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9f648-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="9f648-107">O cmdlet instala a extensão do Azure Enhanced Monitoring (AEM) que coleta os dados de desempenho e o torna detectável para o sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="9f648-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="9f648-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f648-108">EXAMPLES</span></span>

### <span data-ttu-id="9f648-109">Exemplo 1: usar a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="9f648-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="9f648-110">Este comando configura a máquina virtual chamada contoso-Server para usar a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="9f648-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="9f648-111">O comando especifica a conta de armazenamento chamada stdstorage.</span><span class="sxs-lookup"><span data-stu-id="9f648-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="9f648-112">OS</span><span class="sxs-lookup"><span data-stu-id="9f648-112">PARAMETERS</span></span>

### <span data-ttu-id="9f648-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f648-113">-DefaultProfile</span></span>
<span data-ttu-id="9f648-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f648-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f648-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="9f648-115">-EnableWAD</span></span>
<span data-ttu-id="9f648-116">Se esse parâmetro for fornecido, o commandlet habilitará o diagnóstico do Windows Azure para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9f648-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="9f648-117">-OSType</span><span class="sxs-lookup"><span data-stu-id="9f648-117">-OSType</span></span>
<span data-ttu-id="9f648-118">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9f648-118">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="9f648-119">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f648-119">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="9f648-120">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="9f648-120">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="9f648-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f648-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f648-122">Especifica o nome do grupo de recursos da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="9f648-122">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9f648-123">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="9f648-123">-SkipStorage</span></span>
<span data-ttu-id="9f648-124">Indica que esse cmdlet ignora a configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="9f648-124">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="9f648-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="9f648-125">-VMName</span></span>
<span data-ttu-id="9f648-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9f648-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9f648-127">Esse cmdlet adiciona a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9f648-127">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9f648-128">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9f648-128">-WADStorageAccountName</span></span>
<span data-ttu-id="9f648-129">Especifica o nome da conta de armazenamento que este cmdlet usa para configurar a extensão LinuxDiagnostics ou IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="9f648-129">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="9f648-130">Se a máquina virtual não usar uma conta de armazenamento padrão, você deve especificar um valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9f648-130">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="9f648-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f648-131">CommonParameters</span></span>
<span data-ttu-id="9f648-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f648-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f648-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f648-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f648-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f648-134">INPUTS</span></span>

### <span data-ttu-id="9f648-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9f648-135">System.String</span></span>

## <span data-ttu-id="9f648-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f648-136">OUTPUTS</span></span>

### <span data-ttu-id="9f648-137">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9f648-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9f648-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f648-138">NOTES</span></span>

## <span data-ttu-id="9f648-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f648-139">RELATED LINKS</span></span>

[<span data-ttu-id="9f648-140">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9f648-140">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="9f648-141">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9f648-141">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="9f648-142">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="9f648-142">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


