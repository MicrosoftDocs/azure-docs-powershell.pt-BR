---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945613"
---
# <span data-ttu-id="6cd93-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="6cd93-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="6cd93-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6cd93-102">SYNOPSIS</span></span>
<span data-ttu-id="6cd93-103">Obtém o namespace.</span><span class="sxs-lookup"><span data-stu-id="6cd93-103">Gets the namespace.</span></span>


## <span data-ttu-id="6cd93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6cd93-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6cd93-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6cd93-105">DESCRIPTION</span></span>
<span data-ttu-id="6cd93-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6cd93-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6cd93-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6cd93-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6cd93-108">O cmdlet **Get-AzureSBNamespace** retorna os namespaces do serviço de barramento do serviço associados à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6cd93-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="6cd93-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6cd93-109">EXAMPLES</span></span>

### <span data-ttu-id="6cd93-110">Exemplo 1: obter o namespace do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="6cd93-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="6cd93-111">Este exemplo obtém os namespaces do serviço de barramento do serviço associados à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="6cd93-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="6cd93-112">OS</span><span class="sxs-lookup"><span data-stu-id="6cd93-112">PARAMETERS</span></span>

### <span data-ttu-id="6cd93-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cd93-113">-Name</span></span>
<span data-ttu-id="6cd93-114">Especifica o nome de um namespace de barramento de serviço a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="6cd93-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="6cd93-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="6cd93-115">-Profile</span></span>
<span data-ttu-id="6cd93-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="6cd93-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6cd93-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="6cd93-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6cd93-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cd93-118">CommonParameters</span></span>
<span data-ttu-id="6cd93-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cd93-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cd93-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cd93-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cd93-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6cd93-121">INPUTS</span></span>

## <span data-ttu-id="6cd93-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6cd93-122">OUTPUTS</span></span>

## <span data-ttu-id="6cd93-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6cd93-123">NOTES</span></span>

## <span data-ttu-id="6cd93-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6cd93-124">RELATED LINKS</span></span>

[<span data-ttu-id="6cd93-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="6cd93-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


