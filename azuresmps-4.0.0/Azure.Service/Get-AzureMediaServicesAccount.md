---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1327796-0CDC-43E0-97A6-FD1BF570066F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c8676fbf957ebe96f0e849eedd3f64aca19a7741
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946335"
---
# <span data-ttu-id="74e49-101">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="74e49-101">Get-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="74e49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74e49-102">SYNOPSIS</span></span>
<span data-ttu-id="74e49-103">Obtém as contas dos serviços de mídia do Azure disponíveis.</span><span class="sxs-lookup"><span data-stu-id="74e49-103">Gets the available Azure Media Services accounts.</span></span>

<span data-ttu-id="74e49-104">**Observação:** Esta versão foi preterida, confira a [versão mais recente](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="74e49-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="74e49-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74e49-105">SYNTAX</span></span>

```
Get-AzureMediaServicesAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74e49-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74e49-106">DESCRIPTION</span></span>
<span data-ttu-id="74e49-107">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="74e49-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="74e49-108">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="74e49-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="74e49-109">Para listar todas as contas, use o `Get-AzureMediaServicesAccount` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74e49-109">To list all the accounts, use the `Get-AzureMediaServicesAccount` cmdlet.</span></span>
<span data-ttu-id="74e49-110">Para obter informações mais detalhadas sobre uma conta específica, use o `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74e49-110">To get more detailed information about a specific account, use the `Get-AzureMediaServicesAccount -Name YourAccountName` cmdlet.</span></span>

## <span data-ttu-id="74e49-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74e49-111">EXAMPLES</span></span>

### <span data-ttu-id="74e49-112">Exemplo 1: listar todas as contas de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="74e49-112">Example 1: List all Media Services accounts</span></span>
```
PS C:\> Get-AzureMediaServicesAccount
```

<span data-ttu-id="74e49-113">Esse comando lista todas as contas de serviços de mídia disponíveis.</span><span class="sxs-lookup"><span data-stu-id="74e49-113">This command lists all available Media Services accounts.</span></span>

### <span data-ttu-id="74e49-114">Exemplo 2: obter informações detalhadas sobre uma conta de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="74e49-114">Example 2: Get detailed information about a Media Services account</span></span>
```
PS C:\> Get-AzureMediaServicesAccount -Name accountname
```

<span data-ttu-id="74e49-115">Esse comando exibe as propriedades de uma conta de serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="74e49-115">This command displays properties of a Media Services account.</span></span>

## <span data-ttu-id="74e49-116">OS</span><span class="sxs-lookup"><span data-stu-id="74e49-116">PARAMETERS</span></span>

### <span data-ttu-id="74e49-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="74e49-117">-Name</span></span>
<span data-ttu-id="74e49-118">O nome da conta dos serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="74e49-118">The Media Services account name.</span></span>

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

### <span data-ttu-id="74e49-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="74e49-119">-Profile</span></span>
<span data-ttu-id="74e49-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="74e49-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74e49-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="74e49-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74e49-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e49-122">CommonParameters</span></span>
<span data-ttu-id="74e49-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e49-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e49-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e49-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e49-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74e49-125">INPUTS</span></span>

## <span data-ttu-id="74e49-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74e49-126">OUTPUTS</span></span>

## <span data-ttu-id="74e49-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74e49-127">NOTES</span></span>

## <span data-ttu-id="74e49-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74e49-128">RELATED LINKS</span></span>

[<span data-ttu-id="74e49-129">Como usar o Azure PowerShell para serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="74e49-129">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)


