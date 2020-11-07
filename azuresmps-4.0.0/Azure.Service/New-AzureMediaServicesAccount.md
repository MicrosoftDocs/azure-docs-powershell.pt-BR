---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945911"
---
# <span data-ttu-id="30361-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="30361-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="30361-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30361-102">SYNOPSIS</span></span>
<span data-ttu-id="30361-103">Cria uma conta do Azure Media Services.</span><span class="sxs-lookup"><span data-stu-id="30361-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="30361-104">**Observação:** Esta versão foi preterida, confira a [versão mais recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="30361-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="30361-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30361-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="30361-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30361-106">DESCRIPTION</span></span>
<span data-ttu-id="30361-107">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30361-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="30361-108">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="30361-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="30361-109">O cmdlet **New-AzureMediaServicesAccount** cria uma nova conta de serviços de mídia com o nome da conta de serviços de mídia especificado, o local do Data Center em que você deseja criar a conta e um nome de conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="30361-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="30361-110">A conta de armazenamento precisa estar localizada no mesmo Data Center que a nova conta de serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="30361-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="30361-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30361-111">EXAMPLES</span></span>

### <span data-ttu-id="30361-112">Exemplo 1: criar uma nova conta de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="30361-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="30361-113">OS</span><span class="sxs-lookup"><span data-stu-id="30361-113">PARAMETERS</span></span>

### <span data-ttu-id="30361-114">-Local</span><span class="sxs-lookup"><span data-stu-id="30361-114">-Location</span></span>
<span data-ttu-id="30361-115">Especifica o local do datacenter dos serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="30361-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="30361-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="30361-116">-Name</span></span>
<span data-ttu-id="30361-117">Especifica o nome da conta dos serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="30361-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="30361-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="30361-118">-Profile</span></span>
<span data-ttu-id="30361-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="30361-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="30361-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="30361-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="30361-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="30361-121">-StorageAccountName</span></span>
<span data-ttu-id="30361-122">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="30361-122">Specifies the storage account name.</span></span>
<span data-ttu-id="30361-123">A conta de armazenamento já deve existir no mesmo datacenter que a nova conta de serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="30361-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="30361-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30361-124">CommonParameters</span></span>
<span data-ttu-id="30361-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30361-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30361-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30361-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30361-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30361-127">INPUTS</span></span>

## <span data-ttu-id="30361-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30361-128">OUTPUTS</span></span>

## <span data-ttu-id="30361-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30361-129">NOTES</span></span>

## <span data-ttu-id="30361-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30361-130">RELATED LINKS</span></span>

[<span data-ttu-id="30361-131">Como usar o Azure PowerShell para serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="30361-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="30361-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="30361-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="30361-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="30361-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)


