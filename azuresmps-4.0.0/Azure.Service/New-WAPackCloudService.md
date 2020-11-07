---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947357"
---
# <span data-ttu-id="b17b5-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="b17b5-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="b17b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b17b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b17b5-103">Cria um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b17b5-103">Creates a cloud service.</span></span>

## <span data-ttu-id="b17b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b17b5-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b17b5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b17b5-105">DESCRIPTION</span></span>
<span data-ttu-id="b17b5-106">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="b17b5-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="b17b5-107">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b17b5-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="b17b5-108">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="b17b5-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="b17b5-109">O cmdlet **New-WAPackCloudService** cria um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b17b5-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="b17b5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b17b5-110">EXAMPLES</span></span>

### <span data-ttu-id="b17b5-111">Exemplo 1: criar um serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="b17b5-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="b17b5-112">O comando cria um serviço em nuvem chamado ContosoCloudService01 com um rótulo.</span><span class="sxs-lookup"><span data-stu-id="b17b5-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="b17b5-113">OS</span><span class="sxs-lookup"><span data-stu-id="b17b5-113">PARAMETERS</span></span>

### <span data-ttu-id="b17b5-114">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="b17b5-114">-Label</span></span>
<span data-ttu-id="b17b5-115">Especifica um rótulo para o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b17b5-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="b17b5-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b17b5-116">-Name</span></span>
<span data-ttu-id="b17b5-117">Especifica um nome para o cloudservice.</span><span class="sxs-lookup"><span data-stu-id="b17b5-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="b17b5-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b17b5-118">-Profile</span></span>
<span data-ttu-id="b17b5-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b17b5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b17b5-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b17b5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b17b5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b17b5-121">CommonParameters</span></span>
<span data-ttu-id="b17b5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b17b5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b17b5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b17b5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b17b5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b17b5-124">INPUTS</span></span>

## <span data-ttu-id="b17b5-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b17b5-125">OUTPUTS</span></span>

## <span data-ttu-id="b17b5-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b17b5-126">NOTES</span></span>

## <span data-ttu-id="b17b5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b17b5-127">RELATED LINKS</span></span>

[<span data-ttu-id="b17b5-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="b17b5-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="b17b5-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="b17b5-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


