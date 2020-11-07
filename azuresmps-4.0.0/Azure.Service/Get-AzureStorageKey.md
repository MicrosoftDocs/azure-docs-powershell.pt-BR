---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945548"
---
# <span data-ttu-id="cccec-101">Get-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="cccec-101">Get-AzureStorageKey</span></span>

## <span data-ttu-id="cccec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cccec-102">SYNOPSIS</span></span>
<span data-ttu-id="cccec-103">Retorna as chaves de conta de armazenamento primária e secundária para uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="cccec-103">Returns the primary and secondary storage account keys for an Azure storage account.</span></span>

## <span data-ttu-id="cccec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cccec-104">SYNTAX</span></span>

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cccec-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cccec-105">DESCRIPTION</span></span>
<span data-ttu-id="cccec-106">O cmdlet **Get-AzureStorageKey** retorna um objeto com o nome da conta de armazenamento do Azure, a chave da conta primária e a chave da conta secundária da conta de armazenamento do Azure especificada como propriedades.</span><span class="sxs-lookup"><span data-stu-id="cccec-106">The **Get-AzureStorageKey** cmdlet returns an object with the Azure Storage account name, the primary account key, and the secondary account key of the specified Azure storage account as properties.</span></span>

## <span data-ttu-id="cccec-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cccec-107">EXAMPLES</span></span>

### <span data-ttu-id="cccec-108">Exemplo 1: obter um objeto que contém as chaves de armazenamento principal e secundário</span><span class="sxs-lookup"><span data-stu-id="cccec-108">Example 1: Get an object that contains primary and secondary storage keys</span></span>
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="cccec-109">Esse comando obtém um objeto com as chaves de armazenamento principal e secundário para a conta de armazenamento do ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="cccec-109">This command gets an object with the primary and secondary storage keys for the ContosoStore01 storage account.</span></span>

### <span data-ttu-id="cccec-110">Exemplo 2: obter a chave da conta de armazenamento principal e armazená-la em uma variável</span><span class="sxs-lookup"><span data-stu-id="cccec-110">Example 2: Get the primary storage account key and store it in a variable</span></span>
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

<span data-ttu-id="cccec-111">Esse comando coloca a chave da conta de armazenamento primária da conta de armazenamento do ContosoStore01 na variável $ContosoStoreKey.</span><span class="sxs-lookup"><span data-stu-id="cccec-111">This command puts the primary storage account key for the ContosoStore01 storage account in the $ContosoStoreKey variable.</span></span>

## <span data-ttu-id="cccec-112">OS</span><span class="sxs-lookup"><span data-stu-id="cccec-112">PARAMETERS</span></span>

### <span data-ttu-id="cccec-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cccec-113">-InformationAction</span></span>
<span data-ttu-id="cccec-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cccec-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cccec-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cccec-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cccec-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="cccec-116">Continue</span></span>
- <span data-ttu-id="cccec-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cccec-117">Ignore</span></span>
- <span data-ttu-id="cccec-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="cccec-118">Inquire</span></span>
- <span data-ttu-id="cccec-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cccec-119">SilentlyContinue</span></span>
- <span data-ttu-id="cccec-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="cccec-120">Stop</span></span>
- <span data-ttu-id="cccec-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="cccec-121">Suspend</span></span>

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

### <span data-ttu-id="cccec-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cccec-122">-InformationVariable</span></span>
<span data-ttu-id="cccec-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="cccec-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cccec-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cccec-124">-Profile</span></span>
<span data-ttu-id="cccec-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cccec-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cccec-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cccec-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cccec-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cccec-127">-StorageAccountName</span></span>
<span data-ttu-id="cccec-128">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cccec-128">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cccec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccec-129">CommonParameters</span></span>
<span data-ttu-id="cccec-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccec-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cccec-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccec-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cccec-132">INPUTS</span></span>

## <span data-ttu-id="cccec-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cccec-133">OUTPUTS</span></span>

## <span data-ttu-id="cccec-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cccec-134">NOTES</span></span>
* <span data-ttu-id="cccec-135">Para obter ajuda com Node.js, use o `help node-dev` comando.</span><span class="sxs-lookup"><span data-stu-id="cccec-135">To get help with Node.js, use the `help node-dev` command.</span></span> <span data-ttu-id="cccec-136">Para obter ajuda com as extensões do PHP, use o `help php-dev` comando.</span><span class="sxs-lookup"><span data-stu-id="cccec-136">For help with PHP extensions, use the `help php-dev` command.</span></span>

## <span data-ttu-id="cccec-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cccec-137">RELATED LINKS</span></span>

[<span data-ttu-id="cccec-138">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cccec-138">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="cccec-139">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cccec-139">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="cccec-140">New-AzureStorageKey</span><span class="sxs-lookup"><span data-stu-id="cccec-140">New-AzureStorageKey</span></span>](./New-AzureStorageKey.md)

[<span data-ttu-id="cccec-141">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cccec-141">Remove-AzureStorageAccount</span></span>](./Remove-AzureStorageAccount.md)

[<span data-ttu-id="cccec-142">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cccec-142">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


