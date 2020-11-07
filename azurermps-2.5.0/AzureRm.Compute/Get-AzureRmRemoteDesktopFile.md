---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785567"
---
# <span data-ttu-id="bd58a-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="bd58a-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="bd58a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd58a-102">SYNOPSIS</span></span>
<span data-ttu-id="bd58a-103">Obtém um arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="bd58a-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd58a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd58a-104">SYNTAX</span></span>

### <span data-ttu-id="bd58a-105">Downloads</span><span class="sxs-lookup"><span data-stu-id="bd58a-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd58a-106">Carregar</span><span class="sxs-lookup"><span data-stu-id="bd58a-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd58a-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd58a-107">DESCRIPTION</span></span>
<span data-ttu-id="bd58a-108">O cmdlet **Get-AzureRmRemoteDesktopFile** Obtém um arquivo de protocolo de área de trabalho remota (. RDP).</span><span class="sxs-lookup"><span data-stu-id="bd58a-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="bd58a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd58a-109">EXAMPLES</span></span>

### <span data-ttu-id="bd58a-110">Exemplo 1: obter um arquivo de área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="bd58a-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="bd58a-111">Esse comando obtém o arquivo da área de trabalho remota para a máquina virtual chamada VirtualMachine07.</span><span class="sxs-lookup"><span data-stu-id="bd58a-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="bd58a-112">O comando armazena o resultado no arquivo chamado D:\RemoteDesktopFile07.rdp.</span><span class="sxs-lookup"><span data-stu-id="bd58a-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="bd58a-113">OS</span><span class="sxs-lookup"><span data-stu-id="bd58a-113">PARAMETERS</span></span>

### <span data-ttu-id="bd58a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd58a-114">-DefaultProfile</span></span>
<span data-ttu-id="bd58a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd58a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd58a-116">-Iniciar</span><span class="sxs-lookup"><span data-stu-id="bd58a-116">-Launch</span></span>
<span data-ttu-id="bd58a-117">Indica que esse cmdlet inicia a área de trabalho remota depois de obter o arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="bd58a-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd58a-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="bd58a-118">-LocalPath</span></span>
<span data-ttu-id="bd58a-119">Especifica o caminho completo local em que esse cmdlet armazena o arquivo. rdp.</span><span class="sxs-lookup"><span data-stu-id="bd58a-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd58a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd58a-120">-Name</span></span>
<span data-ttu-id="bd58a-121">Especifica o nome do conjunto de disponibilidade que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="bd58a-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd58a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd58a-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd58a-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bd58a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bd58a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd58a-124">CommonParameters</span></span>
<span data-ttu-id="bd58a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd58a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd58a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd58a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd58a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd58a-127">INPUTS</span></span>

### <span data-ttu-id="bd58a-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bd58a-128">None</span></span>
<span data-ttu-id="bd58a-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bd58a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bd58a-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd58a-130">OUTPUTS</span></span>

## <span data-ttu-id="bd58a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd58a-131">NOTES</span></span>

## <span data-ttu-id="bd58a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd58a-132">RELATED LINKS</span></span>

