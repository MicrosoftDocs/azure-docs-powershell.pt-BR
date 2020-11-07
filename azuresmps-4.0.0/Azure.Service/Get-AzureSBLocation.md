---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03E0442D-248E-41DB-98F5-DB3132CD0DCC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 492abdaab507b3ea5f7a8715c82dc0c29e3e94ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946312"
---
# <span data-ttu-id="df177-101">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="df177-101">Get-AzureSBLocation</span></span>

## <span data-ttu-id="df177-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df177-102">SYNOPSIS</span></span>
<span data-ttu-id="df177-103">Obtém a localização do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="df177-103">Gets the location of the Service Bus.</span></span>

## <span data-ttu-id="df177-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df177-104">SYNTAX</span></span>

```
Get-AzureSBLocation [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df177-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df177-105">DESCRIPTION</span></span>
<span data-ttu-id="df177-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="df177-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="df177-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="df177-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="df177-108">O cmdlet **Get-AzureSBLocation** retorna os locais a partir dos quais o barramento do serviço está disponível.</span><span class="sxs-lookup"><span data-stu-id="df177-108">The **Get-AzureSBLocation** cmdlet returns the locations from which the Service Bus is available.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="df177-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df177-109">EXAMPLES</span></span>

### <span data-ttu-id="df177-110">Exemplo 1: obter o local do barramento do serviço</span><span class="sxs-lookup"><span data-stu-id="df177-110">Example 1: Get the Service Bus location</span></span>
```
PS C:\> Get-AzureSBLocation
```

<span data-ttu-id="df177-111">Este exemplo obtém a localização do barramento do serviço.</span><span class="sxs-lookup"><span data-stu-id="df177-111">This example gets the location of the Service Bus.</span></span>

## <span data-ttu-id="df177-112">OS</span><span class="sxs-lookup"><span data-stu-id="df177-112">PARAMETERS</span></span>

### <span data-ttu-id="df177-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="df177-113">-Profile</span></span>
<span data-ttu-id="df177-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="df177-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="df177-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="df177-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df177-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df177-116">CommonParameters</span></span>
<span data-ttu-id="df177-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df177-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df177-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df177-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df177-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df177-119">INPUTS</span></span>

## <span data-ttu-id="df177-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df177-120">OUTPUTS</span></span>

## <span data-ttu-id="df177-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df177-121">NOTES</span></span>

## <span data-ttu-id="df177-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df177-122">RELATED LINKS</span></span>

[<span data-ttu-id="df177-123">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="df177-123">Get-AzureSBNamespace</span></span>](./Get-AzureSBNamespace.md)


