---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947397"
---
# <span data-ttu-id="bf99d-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="bf99d-101">New-WAPackVNet</span></span>

## <span data-ttu-id="bf99d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf99d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf99d-103">Cria uma rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="bf99d-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="bf99d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf99d-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf99d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf99d-105">DESCRIPTION</span></span>
<span data-ttu-id="bf99d-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="bf99d-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="bf99d-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bf99d-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bf99d-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bf99d-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bf99d-109">O cmdlet **New-WAPackVNet** cria uma rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="bf99d-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="bf99d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf99d-110">EXAMPLES</span></span>

### <span data-ttu-id="bf99d-111">Exemplo 1: criar uma rede virtualizada</span><span class="sxs-lookup"><span data-stu-id="bf99d-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="bf99d-112">Primeiro, o primeiro comando recupera a rede lógica à qual queremos adicionar uma nova rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="bf99d-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="bf99d-113">Essa rede lógica é chamada de ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="bf99d-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="bf99d-114">O segundo comando e o último comando cria uma rede virtualizada usando a rede lógica recuperada anteriormente, um nome (ContosoVNett01) e uma descrição (uma descrição).</span><span class="sxs-lookup"><span data-stu-id="bf99d-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="bf99d-115">OS</span><span class="sxs-lookup"><span data-stu-id="bf99d-115">PARAMETERS</span></span>

### <span data-ttu-id="bf99d-116">-Descrição</span><span class="sxs-lookup"><span data-stu-id="bf99d-116">-Description</span></span>
<span data-ttu-id="bf99d-117">Especifica uma descrição para a rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="bf99d-117">Specifies a description for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf99d-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="bf99d-118">-LogicalNetwork</span></span>
<span data-ttu-id="bf99d-119">Especifica um LogicalNetwork associado à rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="bf99d-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf99d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf99d-120">-Name</span></span>
<span data-ttu-id="bf99d-121">Especifica um nome para a rede virtualizada.</span><span class="sxs-lookup"><span data-stu-id="bf99d-121">Specifies a name for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf99d-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bf99d-122">-Profile</span></span>
<span data-ttu-id="bf99d-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bf99d-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf99d-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bf99d-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf99d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf99d-125">CommonParameters</span></span>
<span data-ttu-id="bf99d-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf99d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf99d-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf99d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf99d-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf99d-128">INPUTS</span></span>

## <span data-ttu-id="bf99d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf99d-129">OUTPUTS</span></span>

## <span data-ttu-id="bf99d-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf99d-130">NOTES</span></span>

## <span data-ttu-id="bf99d-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf99d-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf99d-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="bf99d-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="bf99d-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="bf99d-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


