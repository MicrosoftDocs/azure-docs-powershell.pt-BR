---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117898"
---
# <span data-ttu-id="3f2a1-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="3f2a1-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="3f2a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f2a1-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2a1-103">Obtém os Tipos de Conta de Serviços Cognitivas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="3f2a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f2a1-104">SYNTAX</span></span>

### <span data-ttu-id="3f2a1-105">GetAccountTypes (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3f2a1-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f2a1-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="3f2a1-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f2a1-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f2a1-107">DESCRIPTION</span></span>
<span data-ttu-id="3f2a1-108">O cmdlet **Get-AzCognitiveServicesAccountType** obtém os Tipos de Conta de Serviços Cognitivas disponíveis nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="3f2a1-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f2a1-109">EXAMPLES</span></span>

### <span data-ttu-id="3f2a1-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f2a1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="3f2a1-111">Obter a lista de Tipos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-111">Get the list of available Types.</span></span>

### <span data-ttu-id="3f2a1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3f2a1-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="3f2a1-113">Obter a lista de Tipos disponíveis em westus.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="3f2a1-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="3f2a1-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="3f2a1-115">Verifique se `Face` é um Nome de Tipo válido, o nome será retornado se for um nome válido.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="3f2a1-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3f2a1-116">PARAMETERS</span></span>

### <span data-ttu-id="3f2a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2a1-117">-DefaultProfile</span></span>
<span data-ttu-id="3f2a1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f2a1-119">-Local</span><span class="sxs-lookup"><span data-stu-id="3f2a1-119">-Location</span></span>
<span data-ttu-id="3f2a1-120">Localização da conta dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="3f2a1-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="3f2a1-121">-TypeName</span></span>
<span data-ttu-id="3f2a1-122">Nome do tipo de conta do Serviço Cognitiva.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="3f2a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2a1-123">CommonParameters</span></span>
<span data-ttu-id="3f2a1-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2a1-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f2a1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2a1-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="3f2a1-126">INPUTS</span></span>

### <span data-ttu-id="3f2a1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3f2a1-127">System.String</span></span>

## <span data-ttu-id="3f2a1-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="3f2a1-128">OUTPUTS</span></span>

### <span data-ttu-id="3f2a1-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3f2a1-129">System.String[]</span></span>

### <span data-ttu-id="3f2a1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3f2a1-130">System.String</span></span>

## <span data-ttu-id="3f2a1-131">Notas</span><span class="sxs-lookup"><span data-stu-id="3f2a1-131">NOTES</span></span>

## <span data-ttu-id="3f2a1-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f2a1-132">RELATED LINKS</span></span>
