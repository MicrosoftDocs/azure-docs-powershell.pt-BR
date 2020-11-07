---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 679452A6-A6CA-4DC8-8E00-09E369505319
online version: ''
schema: 2.0.0
ms.openlocfilehash: 933c6de8e7baa55b2093a7ffc4ac28fede13bb5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946458"
---
# <span data-ttu-id="33820-101">Remove-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33820-101">Remove-AzureStorageAccount</span></span>

## <span data-ttu-id="33820-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33820-102">SYNOPSIS</span></span>
<span data-ttu-id="33820-103">Exclui a conta de armazenamento especificada de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="33820-103">Deletes the specified storage account from a subscription.</span></span>

## <span data-ttu-id="33820-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33820-104">SYNTAX</span></span>

```
Remove-AzureStorageAccount [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="33820-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33820-105">DESCRIPTION</span></span>
<span data-ttu-id="33820-106">O cmdlet **Remove-AzureStorageAccount** remove uma conta de uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="33820-106">The **Remove-AzureStorageAccount** cmdlet removes an account from an Azure subscription.</span></span>

## <span data-ttu-id="33820-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33820-107">EXAMPLES</span></span>

### <span data-ttu-id="33820-108">Exemplo 1: remover uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="33820-108">Example 1: Remove a storage account</span></span>
```
PS C:\> Remove-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

<span data-ttu-id="33820-109">Este comando Remove a conta de armazenamento ContosoStore01 da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="33820-109">This command removes the ContosoStore01 storage account from the specified subscription.</span></span>

## <span data-ttu-id="33820-110">OS</span><span class="sxs-lookup"><span data-stu-id="33820-110">PARAMETERS</span></span>

### <span data-ttu-id="33820-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="33820-111">-InformationAction</span></span>
<span data-ttu-id="33820-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="33820-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="33820-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="33820-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33820-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="33820-114">Continue</span></span>
- <span data-ttu-id="33820-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="33820-115">Ignore</span></span>
- <span data-ttu-id="33820-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="33820-116">Inquire</span></span>
- <span data-ttu-id="33820-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="33820-117">SilentlyContinue</span></span>
- <span data-ttu-id="33820-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="33820-118">Stop</span></span>
- <span data-ttu-id="33820-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="33820-119">Suspend</span></span>

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

### <span data-ttu-id="33820-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="33820-120">-InformationVariable</span></span>
<span data-ttu-id="33820-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="33820-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="33820-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="33820-122">-Profile</span></span>
<span data-ttu-id="33820-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="33820-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33820-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="33820-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33820-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="33820-125">-StorageAccountName</span></span>
<span data-ttu-id="33820-126">Especifica o nome da conta de armazenamento a ser removida.</span><span class="sxs-lookup"><span data-stu-id="33820-126">Specifies the name of the storage account to remove.</span></span>

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

### <span data-ttu-id="33820-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33820-127">CommonParameters</span></span>
<span data-ttu-id="33820-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33820-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33820-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33820-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33820-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33820-130">INPUTS</span></span>

## <span data-ttu-id="33820-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33820-131">OUTPUTS</span></span>

## <span data-ttu-id="33820-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33820-132">NOTES</span></span>

## <span data-ttu-id="33820-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33820-133">RELATED LINKS</span></span>

[<span data-ttu-id="33820-134">Get-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33820-134">Get-AzureStorageAccount</span></span>](./Get-AzureStorageAccount.md)

[<span data-ttu-id="33820-135">New-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33820-135">New-AzureStorageAccount</span></span>](./New-AzureStorageAccount.md)

[<span data-ttu-id="33820-136">Set-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="33820-136">Set-AzureStorageAccount</span></span>](./Set-AzureStorageAccount.md)


