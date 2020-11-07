---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAEMExtension.md
ms.openlocfilehash: b476254d5b9236aa95a30832499aca65a8a110c0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941439"
---
# <span data-ttu-id="7aa0d-101">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7aa0d-101">Set-AzVMAEMExtension</span></span>

## <span data-ttu-id="7aa0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7aa0d-102">SYNOPSIS</span></span>
<span data-ttu-id="7aa0d-103">Habilita o suporte para monitoramento de sistemas SAP.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-103">Enables support for monitoring for SAP systems.</span></span>

## <span data-ttu-id="7aa0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7aa0d-104">SYNTAX</span></span>

```
Set-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [-NoWait]
 [-SetAccessToIndividualResources] [-InstallNewExtension] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7aa0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7aa0d-105">DESCRIPTION</span></span>
<span data-ttu-id="7aa0d-106">O cmdlet **set-AzVMAEMExtension** atualiza a configuração de uma máquina virtual para habilitar ou atualizar o suporte para o monitoramento de sistemas SAP instalados na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-106">The **Set-AzVMAEMExtension** cmdlet updates the configuration of a virtual machine to enable or update the support for monitoring for SAP systems that are installed on the virtual machine.</span></span>
<span data-ttu-id="7aa0d-107">O cmdlet instala a extensão do Azure Enhanced Monitoring (AEM) que coleta os dados de desempenho e o torna detectável para o sistema SAP.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-107">The cmdlet installs the Azure Enhanced Monitoring (AEM) extension that collects the performance data and makes it discoverable for the SAP system.</span></span>

## <span data-ttu-id="7aa0d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7aa0d-108">EXAMPLES</span></span>

### <span data-ttu-id="7aa0d-109">Exemplo 1: usar a extensão do AEM</span><span class="sxs-lookup"><span data-stu-id="7aa0d-109">Example 1: Use AEM extension</span></span>
```
PS C:\> Set-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

<span data-ttu-id="7aa0d-110">Este comando configura a máquina virtual chamada contoso-Server para usar a extensão do AEM.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-110">This command configures the virtual machine named contoso-server to use the AEM extension.</span></span>
<span data-ttu-id="7aa0d-111">O comando especifica a conta de armazenamento chamada stdstorage.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-111">The command specifies the storage account named stdstorage.</span></span>

## <span data-ttu-id="7aa0d-112">OS</span><span class="sxs-lookup"><span data-stu-id="7aa0d-112">PARAMETERS</span></span>

### <span data-ttu-id="7aa0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7aa0d-113">-DefaultProfile</span></span>
<span data-ttu-id="7aa0d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7aa0d-115">-EnableWAD</span><span class="sxs-lookup"><span data-stu-id="7aa0d-115">-EnableWAD</span></span>
<span data-ttu-id="7aa0d-116">Se esse parâmetro for fornecido, o commandlet habilitará o diagnóstico do Windows Azure para esta máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-116">If this parameter is provided, the commandlet will enable Windows Azure Diagnostics for this virtual machine.</span></span>

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

### <span data-ttu-id="7aa0d-117">-InstallNewExtension</span><span class="sxs-lookup"><span data-stu-id="7aa0d-117">-InstallNewExtension</span></span>
<span data-ttu-id="7aa0d-118">Instale a nova extensão de VM para SAP.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-118">Install the new VM Extension for SAP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa0d-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="7aa0d-119">-NoWait</span></span>
<span data-ttu-id="7aa0d-120">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-120">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7aa0d-121">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-121">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7aa0d-122">-OSType</span><span class="sxs-lookup"><span data-stu-id="7aa0d-122">-OSType</span></span>
<span data-ttu-id="7aa0d-123">Especifica o tipo de sistema operacional do disco do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-123">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="7aa0d-124">Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-124">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="7aa0d-125">Os valores aceitáveis para esse parâmetro são: Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-125">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="7aa0d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7aa0d-126">-ResourceGroupName</span></span>
<span data-ttu-id="7aa0d-127">Especifica o nome do grupo de recursos da máquina virtual que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-127">Specifies the name of the resource group of the virtual machine that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7aa0d-128">-SetAccessToIndividualResources</span><span class="sxs-lookup"><span data-stu-id="7aa0d-128">-SetAccessToIndividualResources</span></span>
<span data-ttu-id="7aa0d-129">Define o acesso da identidade da VM para os recursos individuais, por exemplo, discos de dados em vez do grupo de recursos completo.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-129">Sets the access of the VM identity to the individual resources, e.g. data disks instead of the complete resource group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7aa0d-130">-SkipStorage</span><span class="sxs-lookup"><span data-stu-id="7aa0d-130">-SkipStorage</span></span>
<span data-ttu-id="7aa0d-131">Indica que esse cmdlet ignora a configuração de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-131">Indicates that this cmdlet skips configuration of storage.</span></span>

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

### <span data-ttu-id="7aa0d-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="7aa0d-132">-VMName</span></span>
<span data-ttu-id="7aa0d-133">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7aa0d-134">Esse cmdlet adiciona a extensão do AEM para a máquina virtual que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-134">This cmdlet adds the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7aa0d-135">-WADStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7aa0d-135">-WADStorageAccountName</span></span>
<span data-ttu-id="7aa0d-136">Especifica o nome da conta de armazenamento que este cmdlet usa para configurar a extensão LinuxDiagnostics ou IaaSDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-136">Specifies the name of the storage account that this cmdlet uses to configure the LinuxDiagnostics or IaaSDiagnostics extension.</span></span>
<span data-ttu-id="7aa0d-137">Se a máquina virtual não usar uma conta de armazenamento padrão, você deve especificar um valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-137">If the virtual machine does not use a standard storage account, you must specify a value for this parameter.</span></span>

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

### <span data-ttu-id="7aa0d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7aa0d-138">CommonParameters</span></span>
<span data-ttu-id="7aa0d-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7aa0d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7aa0d-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7aa0d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7aa0d-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7aa0d-141">INPUTS</span></span>

### <span data-ttu-id="7aa0d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7aa0d-142">System.String</span></span>

## <span data-ttu-id="7aa0d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7aa0d-143">OUTPUTS</span></span>

### <span data-ttu-id="7aa0d-144">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7aa0d-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7aa0d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7aa0d-145">NOTES</span></span>

## <span data-ttu-id="7aa0d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7aa0d-146">RELATED LINKS</span></span>

[<span data-ttu-id="7aa0d-147">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7aa0d-147">Get-AzVMAEMExtension</span></span>](./Get-AzVMAEMExtension.md)

[<span data-ttu-id="7aa0d-148">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7aa0d-148">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="7aa0d-149">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7aa0d-149">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


