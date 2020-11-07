---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947353"
---
# <span data-ttu-id="3bb86-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3bb86-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="3bb86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3bb86-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb86-103">Obtém objetos de serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3bb86-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="3bb86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bb86-104">SYNTAX</span></span>

### <span data-ttu-id="3bb86-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="3bb86-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3bb86-106">FromName</span><span class="sxs-lookup"><span data-stu-id="3bb86-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3bb86-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3bb86-107">DESCRIPTION</span></span>
<span data-ttu-id="3bb86-108">Esses tópicos são preteridos e serão removidos no futuro.</span><span class="sxs-lookup"><span data-stu-id="3bb86-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="3bb86-109">Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3bb86-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3bb86-110">Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3bb86-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3bb86-111">O cmdlet **Get-WAPackCloudService** obtém objetos de serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3bb86-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="3bb86-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3bb86-112">EXAMPLES</span></span>

## <span data-ttu-id="3bb86-113">OS</span><span class="sxs-lookup"><span data-stu-id="3bb86-113">PARAMETERS</span></span>

### <span data-ttu-id="3bb86-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bb86-114">-Name</span></span>
<span data-ttu-id="3bb86-115">Especifica o nome de um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="3bb86-115">Specifies the name of a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb86-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3bb86-116">-Profile</span></span>
<span data-ttu-id="3bb86-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3bb86-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3bb86-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3bb86-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3bb86-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb86-119">CommonParameters</span></span>
<span data-ttu-id="3bb86-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb86-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb86-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb86-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb86-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3bb86-122">INPUTS</span></span>

## <span data-ttu-id="3bb86-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3bb86-123">OUTPUTS</span></span>

## <span data-ttu-id="3bb86-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3bb86-124">NOTES</span></span>

## <span data-ttu-id="3bb86-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3bb86-125">RELATED LINKS</span></span>

[<span data-ttu-id="3bb86-126">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3bb86-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="3bb86-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="3bb86-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


