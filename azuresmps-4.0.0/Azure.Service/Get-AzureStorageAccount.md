---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945549"
---
# <span data-ttu-id="79b1f-101">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b1f-101">Get-AzureStorageAccount</span></span>

## <span data-ttu-id="79b1f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79b1f-102">SYNOPSIS</span></span>
<span data-ttu-id="79b1f-103">Obtém as contas de armazenamento para a assinatura atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="79b1f-103">Gets the storage accounts for the current Azure subscription.</span></span>

## <span data-ttu-id="79b1f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79b1f-104">SYNTAX</span></span>

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="79b1f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79b1f-105">DESCRIPTION</span></span>
<span data-ttu-id="79b1f-106">O cmdlet **Get-AzureStorageAccount** retorna um objeto que contém informações sobre as contas de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="79b1f-106">The **Get-AzureStorageAccount** cmdlet returns an object containing information about the storage accounts for the current subscription.</span></span>
<span data-ttu-id="79b1f-107">Se o parâmetro *StorageAccountName* for especificado, apenas informações sobre a conta de armazenamento especificada serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="79b1f-107">If the *StorageAccountName* parameter is specified, then only information about the specified storage account is returned.</span></span>

## <span data-ttu-id="79b1f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79b1f-108">EXAMPLES</span></span>

### <span data-ttu-id="79b1f-109">Exemplo 1: retornar todas as contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="79b1f-109">Example 1: Return all storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount
```

<span data-ttu-id="79b1f-110">Esse comando retorna um objeto com todas as contas de armazenamento associadas à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="79b1f-110">This command returns an object with all the storage accounts associated with the current subscription.</span></span>

### <span data-ttu-id="79b1f-111">Exemplo 2: retornar informações da conta para uma conta especificada</span><span class="sxs-lookup"><span data-stu-id="79b1f-111">Example 2: Return account information for a specified account</span></span>
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="79b1f-112">Esse comando retorna um objeto com apenas as informações da conta do ContosoStore01.</span><span class="sxs-lookup"><span data-stu-id="79b1f-112">This command returns an object with only the ContosoStore01 account information.</span></span>

### <span data-ttu-id="79b1f-113">Exemplo 3: exibir uma tabela de contas de armazenamento</span><span class="sxs-lookup"><span data-stu-id="79b1f-113">Example 3: Display a table of storage accounts</span></span>
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

<span data-ttu-id="79b1f-114">Esse comando retorna um objeto com todas as contas de armazenamento associadas à assinatura atual e os gera como uma tabela que mostra o nome da conta, o rótulo da conta e o local de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="79b1f-114">This command returns an object with all the storage accounts associated with the current subscription, and outputs them as a table showing the account name, the account label, and the storage location.</span></span>

## <span data-ttu-id="79b1f-115">OS</span><span class="sxs-lookup"><span data-stu-id="79b1f-115">PARAMETERS</span></span>

### <span data-ttu-id="79b1f-116">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="79b1f-116">-InformationAction</span></span>
<span data-ttu-id="79b1f-117">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="79b1f-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="79b1f-118">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="79b1f-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79b1f-119">Contínuo</span><span class="sxs-lookup"><span data-stu-id="79b1f-119">Continue</span></span>
- <span data-ttu-id="79b1f-120">Ignorar</span><span class="sxs-lookup"><span data-stu-id="79b1f-120">Ignore</span></span>
- <span data-ttu-id="79b1f-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="79b1f-121">Inquire</span></span>
- <span data-ttu-id="79b1f-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="79b1f-122">SilentlyContinue</span></span>
- <span data-ttu-id="79b1f-123">Finaliza</span><span class="sxs-lookup"><span data-stu-id="79b1f-123">Stop</span></span>
- <span data-ttu-id="79b1f-124">Suspensão</span><span class="sxs-lookup"><span data-stu-id="79b1f-124">Suspend</span></span>

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

### <span data-ttu-id="79b1f-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="79b1f-125">-InformationVariable</span></span>
<span data-ttu-id="79b1f-126">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="79b1f-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="79b1f-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="79b1f-127">-Profile</span></span>
<span data-ttu-id="79b1f-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="79b1f-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="79b1f-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="79b1f-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="79b1f-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79b1f-130">-StorageAccountName</span></span>
<span data-ttu-id="79b1f-131">Especifica o nome de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="79b1f-131">Specifies the name of a storage account.</span></span>
<span data-ttu-id="79b1f-132">Se especificado, esse cmdlet retornará apenas o objeto da conta de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="79b1f-132">If specified, this cmdlet returns only the specified storage account object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b1f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b1f-133">CommonParameters</span></span>
<span data-ttu-id="79b1f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b1f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b1f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79b1f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b1f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79b1f-136">INPUTS</span></span>

## <span data-ttu-id="79b1f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79b1f-137">OUTPUTS</span></span>

### <span data-ttu-id="79b1f-138">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="79b1f-138">ManagementOperationContext</span></span>

## <span data-ttu-id="79b1f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79b1f-139">NOTES</span></span>
* <span data-ttu-id="79b1f-140">Digite `help node-dev` para obter ajuda sobre cmdlets relacionados a desenvolvimento Node.js.</span><span class="sxs-lookup"><span data-stu-id="79b1f-140">Type `help node-dev` to get help on Node.js development-related cmdlets.</span></span> <span data-ttu-id="79b1f-141">Digite `help php-dev` para obter ajuda sobre cmdlets relacionados ao desenvolvimento PHP.</span><span class="sxs-lookup"><span data-stu-id="79b1f-141">Type `help php-dev` to get help on PHP development-related cmdlets.</span></span>

## <span data-ttu-id="79b1f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79b1f-142">RELATED LINKS</span></span>

[<span data-ttu-id="79b1f-143">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b1f-143">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="79b1f-144">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79b1f-144">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


