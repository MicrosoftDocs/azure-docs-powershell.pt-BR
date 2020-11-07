---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: fe6f65aa2e673007b3eda52134c42782c7a49bd9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777037"
---
# <span data-ttu-id="a3eb2-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a3eb2-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="a3eb2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3eb2-103">Obtém informações sobre uma extensão do chefe.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="a3eb2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3eb2-104">SYNTAX</span></span>

### <span data-ttu-id="a3eb2-105">Linux</span><span class="sxs-lookup"><span data-stu-id="a3eb2-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3eb2-106">Windows</span><span class="sxs-lookup"><span data-stu-id="a3eb2-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3eb2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3eb2-107">DESCRIPTION</span></span>
<span data-ttu-id="a3eb2-108">O cmdlet **Get-AzureVMChefExtension** Obtém informações sobre uma extensão chefe instalada em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="a3eb2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3eb2-109">EXAMPLES</span></span>

### <span data-ttu-id="a3eb2-110">Exemplo 1: obter os detalhes da extensão chefe para um computador virtual do Windows-</span><span class="sxs-lookup"><span data-stu-id="a3eb2-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="a3eb2-111">Esse comando obtém a extensão chefe de um computador virtual do Windows chamado WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="a3eb2-112">Exemplo 2: obter os detalhes da extensão chefe para um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="a3eb2-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="a3eb2-113">Esse comando obtém a extensão chefe de um computador virtual Linux chamado LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="a3eb2-114">OS</span><span class="sxs-lookup"><span data-stu-id="a3eb2-114">PARAMETERS</span></span>

### <span data-ttu-id="a3eb2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3eb2-115">-DefaultProfile</span></span>
<span data-ttu-id="a3eb2-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3eb2-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="a3eb2-117">-Linux</span></span>
<span data-ttu-id="a3eb2-118">Indica que esse cmdlet funciona em uma máquina virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3eb2-119">-Name</span></span>
<span data-ttu-id="a3eb2-120">Especifica o nome da extensão do chefe.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-120">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3eb2-121">-ResourceGroupName</span></span>
<span data-ttu-id="a3eb2-122">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="a3eb2-123">-Status</span><span class="sxs-lookup"><span data-stu-id="a3eb2-123">-Status</span></span>
<span data-ttu-id="a3eb2-124">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb2-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="a3eb2-125">-VMName</span></span>
<span data-ttu-id="a3eb2-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="a3eb2-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="a3eb2-127">-Windows</span></span>
<span data-ttu-id="a3eb2-128">Indica que esse cmdlet é para um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3eb2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3eb2-129">CommonParameters</span></span>
<span data-ttu-id="a3eb2-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3eb2-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3eb2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3eb2-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3eb2-132">INPUTS</span></span>

### <span data-ttu-id="a3eb2-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a3eb2-133">None</span></span>
<span data-ttu-id="a3eb2-134">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a3eb2-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3eb2-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3eb2-135">OUTPUTS</span></span>

### <span data-ttu-id="a3eb2-136">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a3eb2-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="a3eb2-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3eb2-137">NOTES</span></span>

## <span data-ttu-id="a3eb2-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3eb2-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3eb2-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a3eb2-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="a3eb2-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="a3eb2-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


