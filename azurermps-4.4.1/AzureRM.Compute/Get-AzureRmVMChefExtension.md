---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMChefExtension.md
ms.openlocfilehash: 2aa0c6516614adb5fae84e2d141cf1882de71628
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611138"
---
# <span data-ttu-id="f91c3-101">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f91c3-101">Get-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="f91c3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f91c3-102">SYNOPSIS</span></span>
<span data-ttu-id="f91c3-103">Obtém informações sobre uma extensão do chefe.</span><span class="sxs-lookup"><span data-stu-id="f91c3-103">Gets information about a Chef extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f91c3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f91c3-104">SYNTAX</span></span>

### <span data-ttu-id="f91c3-105">Linux</span><span class="sxs-lookup"><span data-stu-id="f91c3-105">Linux</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Linux] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f91c3-106">Windows</span><span class="sxs-lookup"><span data-stu-id="f91c3-106">Windows</span></span>
```
Get-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-Windows] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f91c3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f91c3-107">DESCRIPTION</span></span>
<span data-ttu-id="f91c3-108">O cmdlet **Get-AzureVMChefExtension** Obtém informações sobre uma extensão chefe instalada em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f91c3-108">The **Get-AzureVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="f91c3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f91c3-109">EXAMPLES</span></span>

### <span data-ttu-id="f91c3-110">Exemplo 1: obter os detalhes da extensão chefe para um computador virtual do Windows-</span><span class="sxs-lookup"><span data-stu-id="f91c3-110">Example 1: Get the details of Chef extension for a Windows virtual machine-</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="f91c3-111">Esse comando obtém a extensão chefe de um computador virtual do Windows chamado WindowsVM001 que pertence ao grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="f91c3-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f91c3-112">Exemplo 2: obter os detalhes da extensão chefe para um computador virtual Linux</span><span class="sxs-lookup"><span data-stu-id="f91c3-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="f91c3-113">Esse comando obtém a extensão chefe de um computador virtual Linux chamado LinuxVM001 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="f91c3-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f91c3-114">OS</span><span class="sxs-lookup"><span data-stu-id="f91c3-114">PARAMETERS</span></span>

### <span data-ttu-id="f91c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91c3-115">-DefaultProfile</span></span>
<span data-ttu-id="f91c3-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f91c3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f91c3-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="f91c3-117">-Linux</span></span>
<span data-ttu-id="f91c3-118">Indica que esse cmdlet funciona em uma máquina virtual Linux.</span><span class="sxs-lookup"><span data-stu-id="f91c3-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91c3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f91c3-119">-Name</span></span>
<span data-ttu-id="f91c3-120">Especifica o nome da extensão do chefe.</span><span class="sxs-lookup"><span data-stu-id="f91c3-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="f91c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="f91c3-122">Especifica o nome do grupo de recursos que contém a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f91c3-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f91c3-123">-Status</span><span class="sxs-lookup"><span data-stu-id="f91c3-123">-Status</span></span>
<span data-ttu-id="f91c3-124">Indica que esse cmdlet obtém apenas o modo de exibição de instância da extensão chefe.</span><span class="sxs-lookup"><span data-stu-id="f91c3-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f91c3-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f91c3-125">-VMName</span></span>
<span data-ttu-id="f91c3-126">Especifica o nome de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f91c3-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="f91c3-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="f91c3-127">-Windows</span></span>
<span data-ttu-id="f91c3-128">Indica que esse cmdlet é para um computador virtual do Windows.</span><span class="sxs-lookup"><span data-stu-id="f91c3-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f91c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91c3-129">CommonParameters</span></span>
<span data-ttu-id="f91c3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f91c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91c3-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f91c3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91c3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f91c3-132">INPUTS</span></span>

## <span data-ttu-id="f91c3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f91c3-133">OUTPUTS</span></span>

## <span data-ttu-id="f91c3-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f91c3-134">NOTES</span></span>

## <span data-ttu-id="f91c3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f91c3-135">RELATED LINKS</span></span>

[<span data-ttu-id="f91c3-136">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f91c3-136">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)

[<span data-ttu-id="f91c3-137">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f91c3-137">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)


