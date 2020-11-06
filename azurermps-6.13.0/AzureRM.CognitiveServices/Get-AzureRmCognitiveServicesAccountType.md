---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432786"
---
# <span data-ttu-id="30939-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="30939-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="30939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="30939-102">SYNOPSIS</span></span>
<span data-ttu-id="30939-103">Obtém os tipos de conta de serviços cognitivas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="30939-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30939-104">SYNTAX</span></span>

### <span data-ttu-id="30939-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="30939-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30939-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="30939-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30939-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="30939-107">DESCRIPTION</span></span>
<span data-ttu-id="30939-108">O cmdlet **Get-AzureRmCognitiveServicesAccountType** Obtém os tipos de conta de serviços cognitivas disponíveis nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="30939-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="30939-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30939-109">EXAMPLES</span></span>

### <span data-ttu-id="30939-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="30939-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="30939-111">Obter a lista de tipos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="30939-111">Get the list of available Types.</span></span>

### <span data-ttu-id="30939-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="30939-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="30939-113">Obter a lista de tipos disponíveis na westus.</span><span class="sxs-lookup"><span data-stu-id="30939-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="30939-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="30939-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="30939-115">Verifique se `Face` é um nome de tipo válido, o nome será retornado se for um nome válido.</span><span class="sxs-lookup"><span data-stu-id="30939-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="30939-116">OS</span><span class="sxs-lookup"><span data-stu-id="30939-116">PARAMETERS</span></span>

### <span data-ttu-id="30939-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30939-117">-DefaultProfile</span></span>
<span data-ttu-id="30939-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="30939-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30939-119">-Local</span><span class="sxs-lookup"><span data-stu-id="30939-119">-Location</span></span>
<span data-ttu-id="30939-120">Localização da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="30939-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30939-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="30939-121">-TypeName</span></span>
<span data-ttu-id="30939-122">Nome do tipo de conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="30939-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30939-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30939-123">CommonParameters</span></span>
<span data-ttu-id="30939-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30939-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30939-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30939-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30939-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="30939-126">INPUTS</span></span>

### <span data-ttu-id="30939-127">System. String</span><span class="sxs-lookup"><span data-stu-id="30939-127">System.String</span></span>

## <span data-ttu-id="30939-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="30939-128">OUTPUTS</span></span>

### <span data-ttu-id="30939-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="30939-129">System.String[]</span></span>

### <span data-ttu-id="30939-130">System. String</span><span class="sxs-lookup"><span data-stu-id="30939-130">System.String</span></span>

## <span data-ttu-id="30939-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="30939-131">NOTES</span></span>

## <span data-ttu-id="30939-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30939-132">RELATED LINKS</span></span>
