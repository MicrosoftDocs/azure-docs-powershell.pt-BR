---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945948"
---
# <span data-ttu-id="e136f-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="e136f-101">Show-AzurePortal</span></span>

## <span data-ttu-id="e136f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e136f-102">SYNOPSIS</span></span>
<span data-ttu-id="e136f-103">Mostrar o portal de gerenciamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e136f-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="e136f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e136f-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="e136f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e136f-105">DESCRIPTION</span></span>
<span data-ttu-id="e136f-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e136f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e136f-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e136f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e136f-108">O cmdlet **show-AzurePortal** mostra o portal de gerenciamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e136f-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="e136f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e136f-109">EXAMPLES</span></span>

### <span data-ttu-id="e136f-110">Exemplo 1: mostrar informações sobre um site da Web</span><span class="sxs-lookup"><span data-stu-id="e136f-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="e136f-111">Este exemplo abre um navegador no portal do Azure, mostrando informações sobre um site chamado meusite.</span><span class="sxs-lookup"><span data-stu-id="e136f-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="e136f-112">OS</span><span class="sxs-lookup"><span data-stu-id="e136f-112">PARAMETERS</span></span>

### <span data-ttu-id="e136f-113">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="e136f-113">-Environment</span></span>
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

### <span data-ttu-id="e136f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e136f-114">-Name</span></span>
<span data-ttu-id="e136f-115">Especifica o nome do site a ser mostrado no Portal.</span><span class="sxs-lookup"><span data-stu-id="e136f-115">Specifies the name of the website to show in the portal.</span></span>

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

### <span data-ttu-id="e136f-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e136f-116">-Profile</span></span>
<span data-ttu-id="e136f-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e136f-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e136f-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e136f-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e136f-119">-Território</span><span class="sxs-lookup"><span data-stu-id="e136f-119">-Realm</span></span>
<span data-ttu-id="e136f-120">Especifica a ID da organização a ser usada para autenticação federada ao exibir o portal do Azure.</span><span class="sxs-lookup"><span data-stu-id="e136f-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

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

### <span data-ttu-id="e136f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e136f-121">CommonParameters</span></span>
<span data-ttu-id="e136f-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e136f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e136f-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e136f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e136f-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e136f-124">INPUTS</span></span>

## <span data-ttu-id="e136f-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e136f-125">OUTPUTS</span></span>

## <span data-ttu-id="e136f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e136f-126">NOTES</span></span>

## <span data-ttu-id="e136f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e136f-127">RELATED LINKS</span></span>

[<span data-ttu-id="e136f-128">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e136f-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


