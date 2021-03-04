---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: d06f8b5efa0a220b20c5324b457a870d5aaa44b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889018"
---
# <span data-ttu-id="499f8-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="499f8-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="499f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="499f8-102">SYNOPSIS</span></span>
<span data-ttu-id="499f8-103">Obtém um arquivo .rdp.</span><span class="sxs-lookup"><span data-stu-id="499f8-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="499f8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="499f8-104">SYNTAX</span></span>

### <span data-ttu-id="499f8-105">Baixar</span><span class="sxs-lookup"><span data-stu-id="499f8-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="499f8-106">Iniciar</span><span class="sxs-lookup"><span data-stu-id="499f8-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="499f8-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="499f8-107">DESCRIPTION</span></span>
<span data-ttu-id="499f8-108">O cmdlet **Get-AzRemoteDesktopFile** obtém um arquivo Remote Desktop Protocol (.rdp).</span><span class="sxs-lookup"><span data-stu-id="499f8-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="499f8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="499f8-109">EXAMPLES</span></span>

### <span data-ttu-id="499f8-110">Exemplo 1: Obter um arquivo de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="499f8-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="499f8-111">Este comando obtém o arquivo de Área de Trabalho Remota para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="499f8-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="499f8-112">O comando armazena o resultado no arquivo chamado D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="499f8-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="499f8-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="499f8-113">PARAMETERS</span></span>

### <span data-ttu-id="499f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="499f8-114">-DefaultProfile</span></span>
<span data-ttu-id="499f8-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="499f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="499f8-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="499f8-116">-Launch</span></span>
<span data-ttu-id="499f8-117">Indica que esse cmdlet inicia a Área de Trabalho Remota depois que obtém o arquivo .rdp.</span><span class="sxs-lookup"><span data-stu-id="499f8-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="499f8-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="499f8-118">-LocalPath</span></span>
<span data-ttu-id="499f8-119">Especifica o caminho completo local onde esse cmdlet armazena o arquivo .rdp.</span><span class="sxs-lookup"><span data-stu-id="499f8-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499f8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="499f8-120">-Name</span></span>
<span data-ttu-id="499f8-121">Especifica o nome do conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="499f8-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="499f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="499f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="499f8-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="499f8-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="499f8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="499f8-124">CommonParameters</span></span>
<span data-ttu-id="499f8-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="499f8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="499f8-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="499f8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="499f8-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="499f8-127">INPUTS</span></span>

### <span data-ttu-id="499f8-128">System.String</span><span class="sxs-lookup"><span data-stu-id="499f8-128">System.String</span></span>

## <span data-ttu-id="499f8-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="499f8-129">OUTPUTS</span></span>

### <span data-ttu-id="499f8-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="499f8-130">System.Void</span></span>

## <span data-ttu-id="499f8-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="499f8-131">NOTES</span></span>

## <span data-ttu-id="499f8-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="499f8-132">RELATED LINKS</span></span>
