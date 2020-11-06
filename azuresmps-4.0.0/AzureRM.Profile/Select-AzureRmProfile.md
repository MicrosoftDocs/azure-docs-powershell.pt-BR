---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425920"
---
# <span data-ttu-id="ba3e8-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="ba3e8-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="ba3e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3e8-103">Carrega as informações de autenticação do Azure de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="ba3e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba3e8-104">SYNTAX</span></span>

### <span data-ttu-id="ba3e8-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="ba3e8-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="ba3e8-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="ba3e8-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="ba3e8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba3e8-107">DESCRIPTION</span></span>
<span data-ttu-id="ba3e8-108">O cmdlet Select-AzureRmProfile carrega informações de autenticação de um arquivo para definir o contexto e o ambiente do Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="ba3e8-109">Cmdlets que você executa na sessão atual usam essas informações para autenticar solicitações ao Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="ba3e8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba3e8-110">EXAMPLES</span></span>

### <span data-ttu-id="ba3e8-111">Exemplo 1: selecionando um perfil de um PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ba3e8-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="ba3e8-112">Este exemplo seleciona um perfil de um PSAzureProfile que é passado para o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="ba3e8-113">Exemplo 2: selecionando um perfil de um arquivo JSON</span><span class="sxs-lookup"><span data-stu-id="ba3e8-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="ba3e8-114">Este exemplo seleciona um perfil de um arquivo JSON que é passado pelo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="ba3e8-115">Esse arquivo JSON pode ser criado a partir de Save-AzureRmProfile.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="ba3e8-116">OS</span><span class="sxs-lookup"><span data-stu-id="ba3e8-116">PARAMETERS</span></span>

### <span data-ttu-id="ba3e8-117">-Caminho</span><span class="sxs-lookup"><span data-stu-id="ba3e8-117">-Path</span></span>
<span data-ttu-id="ba3e8-118">Especifica o caminho para as informações de perfil salvas usando Save-AzureRMProfile.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3e8-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ba3e8-119">-Profile</span></span>
<span data-ttu-id="ba3e8-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba3e8-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3e8-122">CommonParameters</span></span>
<span data-ttu-id="ba3e8-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3e8-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3e8-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba3e8-125">INPUTS</span></span>

## <span data-ttu-id="ba3e8-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba3e8-126">OUTPUTS</span></span>

### <span data-ttu-id="ba3e8-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="ba3e8-127">PSAzureProfile</span></span>

## <span data-ttu-id="ba3e8-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba3e8-128">NOTES</span></span>

## <span data-ttu-id="ba3e8-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba3e8-129">RELATED LINKS</span></span>

[<span data-ttu-id="ba3e8-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="ba3e8-130">Get-AzureRMContext</span></span>]()

