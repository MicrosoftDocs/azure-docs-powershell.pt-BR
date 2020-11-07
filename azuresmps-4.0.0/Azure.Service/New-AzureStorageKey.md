---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 09ABE9E2-1080-4DEF-92DD-B8FF4C8B308C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9afdaafa57592239d0c24870e4459d650fac84c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946203"
---
# <span data-ttu-id="a09c6-101">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="a09c6-101">New-AzureStorageKey</span></span>

## <span data-ttu-id="a09c6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a09c6-102">SYNOPSIS</span></span>
<span data-ttu-id="a09c6-103">Regenera as chaves de armazenamento para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a09c6-103">Regenerates storage keys for an Azure storage account.</span></span>

## <span data-ttu-id="a09c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a09c6-104">SYNTAX</span></span>

```
New-AzureStorageKey [-KeyType] <String> [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a09c6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a09c6-105">DESCRIPTION</span></span>
<span data-ttu-id="a09c6-106">O cmdlet **New-AzureStorageKey** regenera a chave primária ou secundária para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="a09c6-106">The **New-AzureStorageKey** cmdlet regenerates the primary or secondary key for an Azure Storage account.</span></span>
<span data-ttu-id="a09c6-107">Ele retorna um objeto que contém o nome da conta de armazenamento, a chave primária e a chave secundária como propriedades.</span><span class="sxs-lookup"><span data-stu-id="a09c6-107">It returns an object that contains the storage account name, primary key, and secondary key as properties.</span></span>

## <span data-ttu-id="a09c6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a09c6-108">EXAMPLES</span></span>

### <span data-ttu-id="a09c6-109">Exemplo 1: regenerar uma chave de armazenamento principal</span><span class="sxs-lookup"><span data-stu-id="a09c6-109">Example 1: Regenerate a primary storage key</span></span>
```
PS C:\> New-AzureStorageKey -KeyType "Primary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="a09c6-110">Esse comando regenera a chave de armazenamento principal para a conta de armazenamento do ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="a09c6-110">This command regenerates the primary storage key for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="a09c6-111">Exemplo 2: regenerar uma chave de armazenamento secundário e salvá-la em uma variável</span><span class="sxs-lookup"><span data-stu-id="a09c6-111">Example 2: Regenerate a secondary storage key and save it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = New-AzureStorageKey -KeyType "Secondary" -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="a09c6-112">Esse comando regenera a chave de armazenamento secundário para a conta de armazenamento do ContosoStore01 e armazena as informações da chave da conta de armazenamento atualizada no $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="a09c6-112">This command regenerate the secondary storage key for the ContosoStore01 storage account and stores the updated storage account key information in the $ContosoStoreKey.</span></span>

## <span data-ttu-id="a09c6-113">OS</span><span class="sxs-lookup"><span data-stu-id="a09c6-113">PARAMETERS</span></span>

### <span data-ttu-id="a09c6-114">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a09c6-114">-InformationAction</span></span>
<span data-ttu-id="a09c6-115">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="a09c6-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a09c6-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a09c6-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a09c6-117">Contínuo</span><span class="sxs-lookup"><span data-stu-id="a09c6-117">Continue</span></span>
- <span data-ttu-id="a09c6-118">Ignorar</span><span class="sxs-lookup"><span data-stu-id="a09c6-118">Ignore</span></span>
- <span data-ttu-id="a09c6-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="a09c6-119">Inquire</span></span>
- <span data-ttu-id="a09c6-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a09c6-120">SilentlyContinue</span></span>
- <span data-ttu-id="a09c6-121">Finaliza</span><span class="sxs-lookup"><span data-stu-id="a09c6-121">Stop</span></span>
- <span data-ttu-id="a09c6-122">Suspensão</span><span class="sxs-lookup"><span data-stu-id="a09c6-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09c6-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a09c6-123">-InformationVariable</span></span>
<span data-ttu-id="a09c6-124">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="a09c6-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09c6-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a09c6-125">-KeyType</span></span>
<span data-ttu-id="a09c6-126">Especifica a chave a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="a09c6-126">Specifies which key to regenerate.</span></span>
<span data-ttu-id="a09c6-127">Os valores válidos são: principal e secundário.</span><span class="sxs-lookup"><span data-stu-id="a09c6-127">Valid values are: Primary and Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09c6-128">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a09c6-128">-Profile</span></span>
<span data-ttu-id="a09c6-129">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="a09c6-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a09c6-130">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="a09c6-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a09c6-131">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a09c6-131">-StorageAccountName</span></span>
<span data-ttu-id="a09c6-132">Especifica o nome da conta de armazenamento do Azure para a qual uma chave será regenerada.</span><span class="sxs-lookup"><span data-stu-id="a09c6-132">Specifies the name of the Azure Storage account for which to regenerate a key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09c6-133">CommonParameters</span></span>
<span data-ttu-id="a09c6-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a09c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09c6-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a09c6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09c6-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a09c6-136">INPUTS</span></span>

## <span data-ttu-id="a09c6-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a09c6-137">OUTPUTS</span></span>

### <span data-ttu-id="a09c6-138">StorageServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a09c6-138">StorageServiceKeys</span></span>

## <span data-ttu-id="a09c6-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a09c6-139">NOTES</span></span>

## <span data-ttu-id="a09c6-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a09c6-140">RELATED LINKS</span></span>

[<span data-ttu-id="a09c6-141">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="a09c6-141">Get-AzureStorageKey</span></span>](./Get-AzureStorageKey.md)


