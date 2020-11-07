---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945992"
---
# <span data-ttu-id="52472-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="52472-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="52472-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52472-102">SYNOPSIS</span></span>
<span data-ttu-id="52472-103">Cria modelos de função de trabalho e Web.</span><span class="sxs-lookup"><span data-stu-id="52472-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="52472-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52472-104">SYNTAX</span></span>

### <span data-ttu-id="52472-105">WebRole</span><span class="sxs-lookup"><span data-stu-id="52472-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="52472-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="52472-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52472-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52472-107">DESCRIPTION</span></span>
<span data-ttu-id="52472-108">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52472-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="52472-109">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="52472-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="52472-110">O cmdlet **New-AzureRoleTemplate** cria modelos de função de trabalho e Web.</span><span class="sxs-lookup"><span data-stu-id="52472-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="52472-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52472-111">EXAMPLES</span></span>

### <span data-ttu-id="52472-112">Exemplo 1: criar um modelo de função da Web</span><span class="sxs-lookup"><span data-stu-id="52472-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="52472-113">Este exemplo cria um novo modelo de função da Web em uma pasta chamada webroletemplate no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="52472-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="52472-114">Exemplo 2: criar um modelo de função de trabalhador</span><span class="sxs-lookup"><span data-stu-id="52472-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="52472-115">Este exemplo cria um novo modelo de função de trabalho em uma pasta chamada webroletemplate no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="52472-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="52472-116">Exemplo 3: criar um modelo de função em um diretório personalizado</span><span class="sxs-lookup"><span data-stu-id="52472-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="52472-117">Este exemplo cria um novo modelo de função da Web no diretório chamado MyWebRoleTemplate, em vez de no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="52472-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="52472-118">OS</span><span class="sxs-lookup"><span data-stu-id="52472-118">PARAMETERS</span></span>

### <span data-ttu-id="52472-119">-Saída</span><span class="sxs-lookup"><span data-stu-id="52472-119">-Output</span></span>
<span data-ttu-id="52472-120">Especifica o caminho de saída do modelo gerado.</span><span class="sxs-lookup"><span data-stu-id="52472-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="52472-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="52472-121">-Profile</span></span>
<span data-ttu-id="52472-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="52472-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52472-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="52472-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52472-124">-Web</span><span class="sxs-lookup"><span data-stu-id="52472-124">-Web</span></span>
<span data-ttu-id="52472-125">Especifica que você deseja criar um modelo de função da Web.</span><span class="sxs-lookup"><span data-stu-id="52472-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52472-126">-Trabalhador</span><span class="sxs-lookup"><span data-stu-id="52472-126">-Worker</span></span>
<span data-ttu-id="52472-127">Especifica que você deseja criar um modelo de função de trabalho.</span><span class="sxs-lookup"><span data-stu-id="52472-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52472-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52472-128">CommonParameters</span></span>
<span data-ttu-id="52472-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52472-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52472-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52472-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52472-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52472-131">INPUTS</span></span>

## <span data-ttu-id="52472-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52472-132">OUTPUTS</span></span>

## <span data-ttu-id="52472-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52472-133">NOTES</span></span>

## <span data-ttu-id="52472-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52472-134">RELATED LINKS</span></span>

[<span data-ttu-id="52472-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="52472-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="52472-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="52472-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


