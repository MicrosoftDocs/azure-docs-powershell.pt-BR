---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945937"
---
# <span data-ttu-id="5e807-101">Test-AzureName</span><span class="sxs-lookup"><span data-stu-id="5e807-101">Test-AzureName</span></span>

## <span data-ttu-id="5e807-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5e807-102">SYNOPSIS</span></span>
<span data-ttu-id="5e807-103">Testa se um nome de serviço de nuvem do Microsoft Azure, nome do serviço de armazenamento ou nome do namespace de barramento de serviço existe ou não.</span><span class="sxs-lookup"><span data-stu-id="5e807-103">Tests whether a Microsoft Azure cloud service name, storage service name or service bus namespace name exists or not.</span></span>

## <span data-ttu-id="5e807-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e807-104">SYNTAX</span></span>

### <span data-ttu-id="5e807-105">Atender</span><span class="sxs-lookup"><span data-stu-id="5e807-105">Service</span></span>
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5e807-106">SPS</span><span class="sxs-lookup"><span data-stu-id="5e807-106">Storage</span></span>
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5e807-107">ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5e807-107">ServiceBusNamespace</span></span>
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5e807-108">Site</span><span class="sxs-lookup"><span data-stu-id="5e807-108">Website</span></span>
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e807-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5e807-109">DESCRIPTION</span></span>
<span data-ttu-id="5e807-110">Se o nome existir, o cmdlet retornará $True.</span><span class="sxs-lookup"><span data-stu-id="5e807-110">If the name exists, the cmdlet returns $True.</span></span>
<span data-ttu-id="5e807-111">Se o nome não existir, será retornado $False.</span><span class="sxs-lookup"><span data-stu-id="5e807-111">If the name does not exist, it returns $False.</span></span>

## <span data-ttu-id="5e807-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5e807-112">EXAMPLES</span></span>

### <span data-ttu-id="5e807-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5e807-113">Example 1</span></span>
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

<span data-ttu-id="5e807-114">Esse comando testa se o "MyNameService1" é um nome de serviço de nuvem do Microsoft Azure existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-114">This command tests to see if the "MyNameService1" is an existing Microsoft Azure cloud service name.</span></span>

### <span data-ttu-id="5e807-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5e807-115">Example 2</span></span>
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

<span data-ttu-id="5e807-116">Esse comando testa se o "mystorename1" é um nome de serviço de armazenamento do Microsoft Azure existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-116">This command tests to see if the "mystorename1" is an existing Microsoft Azure storage service name.</span></span>

### <span data-ttu-id="5e807-117">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5e807-117">Example 3</span></span>
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

<span data-ttu-id="5e807-118">Esse comando testa se o "MyNamespace" é um nome de namespace de barramento do serviço do Microsoft Azure existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-118">This command tests to see if the "mynamespace" is an existing Microsoft Azure service bus namespace name.</span></span>

## <span data-ttu-id="5e807-119">OS</span><span class="sxs-lookup"><span data-stu-id="5e807-119">PARAMETERS</span></span>

### <span data-ttu-id="5e807-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e807-120">-Name</span></span>
<span data-ttu-id="5e807-121">Especifica o nome do serviço ou da conta de armazenamento a ser testada.</span><span class="sxs-lookup"><span data-stu-id="5e807-121">Specifies the name of the service or storage account to test.</span></span>

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

### <span data-ttu-id="5e807-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5e807-122">-Profile</span></span>
<span data-ttu-id="5e807-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5e807-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e807-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5e807-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e807-125">-Serviço</span><span class="sxs-lookup"><span data-stu-id="5e807-125">-Service</span></span>
<span data-ttu-id="5e807-126">Especifica o teste para uma conta de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-126">Specifies to test for an existing service account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e807-127">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="5e807-127">-ServiceBusNamespace</span></span>
<span data-ttu-id="5e807-128">Especifica o teste para um namespace de barramento de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-128">Specifies to test for an existing service bus namespace.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e807-129">-Armazenamento</span><span class="sxs-lookup"><span data-stu-id="5e807-129">-Storage</span></span>
<span data-ttu-id="5e807-130">Especifica o teste para uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-130">Specifies to test for an existing storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e807-131">-Website</span><span class="sxs-lookup"><span data-stu-id="5e807-131">-Website</span></span>
<span data-ttu-id="5e807-132">Especifica o teste para um site existente.</span><span class="sxs-lookup"><span data-stu-id="5e807-132">Specifies to test for an existing website.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e807-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e807-133">CommonParameters</span></span>
<span data-ttu-id="5e807-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e807-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e807-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e807-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e807-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5e807-136">INPUTS</span></span>

## <span data-ttu-id="5e807-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5e807-137">OUTPUTS</span></span>

## <span data-ttu-id="5e807-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5e807-138">NOTES</span></span>
* <span data-ttu-id="5e807-139">nó-dev, php-dev, Python-dev</span><span class="sxs-lookup"><span data-stu-id="5e807-139">node-dev, php-dev, python-dev</span></span>

## <span data-ttu-id="5e807-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5e807-140">RELATED LINKS</span></span>

