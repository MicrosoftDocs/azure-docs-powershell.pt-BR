---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 4b3afc0b41f6eaf68e7ec0c4f8ed976b36267c97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427803"
---
# <span data-ttu-id="86add-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="86add-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="86add-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86add-102">SYNOPSIS</span></span>
<span data-ttu-id="86add-103">Verifica a disponibilidade do nome do NameSpace especificado</span><span class="sxs-lookup"><span data-stu-id="86add-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86add-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86add-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86add-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86add-105">DESCRIPTION</span></span>
<span data-ttu-id="86add-106">O cmdlet **Test-AzureRmRelayName** verifica a disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="86add-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="86add-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86add-107">EXAMPLES</span></span>

### <span data-ttu-id="86add-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="86add-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="86add-109">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="86add-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="86add-110">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="86add-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="86add-111">Retorna o status na disponibilidade do nome do namespace</span><span class="sxs-lookup"><span data-stu-id="86add-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="86add-112">OS</span><span class="sxs-lookup"><span data-stu-id="86add-112">PARAMETERS</span></span>

### <span data-ttu-id="86add-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86add-113">-Namespace</span></span>
<span data-ttu-id="86add-114">Nome do namespace de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="86add-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86add-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86add-115">-DefaultProfile</span></span>
<span data-ttu-id="86add-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86add-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86add-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86add-117">CommonParameters</span></span>
<span data-ttu-id="86add-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86add-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86add-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86add-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86add-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86add-120">INPUTS</span></span>

### <span data-ttu-id="86add-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="86add-121">-Namespace</span></span>
 <span data-ttu-id="86add-122">System. String</span><span class="sxs-lookup"><span data-stu-id="86add-122">System.String</span></span>

## <span data-ttu-id="86add-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86add-123">OUTPUTS</span></span>

### <span data-ttu-id="86add-124">[Microsoft. Azure. Commands. Relay. Models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="86add-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="86add-125">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="86add-125">Example 1</span></span>
<span data-ttu-id="86add-126">Mensagem do motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="86add-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="86add-127">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="86add-127">Example 2</span></span>
<span data-ttu-id="86add-128">Mensagem do motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="86add-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="86add-129">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="86add-129">Example 3</span></span>
<span data-ttu-id="86add-130">Mensagem do motivo NameAvailable</span><span class="sxs-lookup"><span data-stu-id="86add-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="86add-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86add-131">NOTES</span></span>

## <span data-ttu-id="86add-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86add-132">RELATED LINKS</span></span>

