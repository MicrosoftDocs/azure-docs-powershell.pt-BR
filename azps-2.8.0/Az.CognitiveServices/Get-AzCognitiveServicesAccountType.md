---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: d5fdae4d60125981b9774fa9b62414c5e3608d73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597547"
---
# <span data-ttu-id="06ec2-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="06ec2-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="06ec2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="06ec2-103">Obtém os tipos de conta de serviços cognitivas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="06ec2-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="06ec2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06ec2-104">SYNTAX</span></span>

### <span data-ttu-id="06ec2-105">GetAccountTypes (padrão)</span><span class="sxs-lookup"><span data-stu-id="06ec2-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06ec2-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="06ec2-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06ec2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="06ec2-108">O cmdlet **Get-AzCognitiveServicesAccountType** Obtém os tipos de conta de serviços cognitivas disponíveis nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="06ec2-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="06ec2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06ec2-109">EXAMPLES</span></span>

### <span data-ttu-id="06ec2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="06ec2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="06ec2-111">Obter a lista de tipos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="06ec2-111">Get the list of available Types.</span></span>

### <span data-ttu-id="06ec2-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="06ec2-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="06ec2-113">Obter a lista de tipos disponíveis na westus.</span><span class="sxs-lookup"><span data-stu-id="06ec2-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="06ec2-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="06ec2-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="06ec2-115">Verifique se `Face` é um nome de tipo válido, o nome será retornado se for um nome válido.</span><span class="sxs-lookup"><span data-stu-id="06ec2-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="06ec2-116">OS</span><span class="sxs-lookup"><span data-stu-id="06ec2-116">PARAMETERS</span></span>

### <span data-ttu-id="06ec2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ec2-117">-DefaultProfile</span></span>
<span data-ttu-id="06ec2-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06ec2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ec2-119">-Local</span><span class="sxs-lookup"><span data-stu-id="06ec2-119">-Location</span></span>
<span data-ttu-id="06ec2-120">Localização da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="06ec2-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="06ec2-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="06ec2-121">-TypeName</span></span>
<span data-ttu-id="06ec2-122">Nome do tipo de conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="06ec2-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="06ec2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ec2-123">CommonParameters</span></span>
<span data-ttu-id="06ec2-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ec2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ec2-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06ec2-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ec2-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06ec2-126">INPUTS</span></span>

### <span data-ttu-id="06ec2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="06ec2-127">System.String</span></span>

## <span data-ttu-id="06ec2-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06ec2-128">OUTPUTS</span></span>

### <span data-ttu-id="06ec2-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="06ec2-129">System.String[]</span></span>

### <span data-ttu-id="06ec2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="06ec2-130">System.String</span></span>

## <span data-ttu-id="06ec2-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06ec2-131">NOTES</span></span>

## <span data-ttu-id="06ec2-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06ec2-132">RELATED LINKS</span></span>
