---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: aacc24926bf38f52f1fd273847e48082c8d110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889038"
---
# <span data-ttu-id="32c63-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="32c63-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="32c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32c63-102">SYNOPSIS</span></span>
<span data-ttu-id="32c63-103">Obtém os Tipos de Conta de Serviços Cognitivos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="32c63-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="32c63-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="32c63-104">SYNTAX</span></span>

### <span data-ttu-id="32c63-105">GetAccountTypes (Padrão)</span><span class="sxs-lookup"><span data-stu-id="32c63-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="32c63-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="32c63-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="32c63-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="32c63-107">DESCRIPTION</span></span>
<span data-ttu-id="32c63-108">O cmdlet **Get-AzCognitiveServicesAccountType** obtém os Tipos de Conta de Serviços Cognitivos disponíveis nesta assinatura.</span><span class="sxs-lookup"><span data-stu-id="32c63-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="32c63-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32c63-109">EXAMPLES</span></span>

### <span data-ttu-id="32c63-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32c63-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="32c63-111">Obter a lista de tipos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="32c63-111">Get the list of available Types.</span></span>

### <span data-ttu-id="32c63-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="32c63-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="32c63-113">Obter a lista de tipos disponíveis em westus.</span><span class="sxs-lookup"><span data-stu-id="32c63-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="32c63-114">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="32c63-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="32c63-115">Verifique se `Face` é um nome de tipo válido, o nome será retornado se for um nome válido.</span><span class="sxs-lookup"><span data-stu-id="32c63-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="32c63-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="32c63-116">PARAMETERS</span></span>

### <span data-ttu-id="32c63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32c63-117">-DefaultProfile</span></span>
<span data-ttu-id="32c63-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="32c63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32c63-119">-Location</span><span class="sxs-lookup"><span data-stu-id="32c63-119">-Location</span></span>
<span data-ttu-id="32c63-120">Local da conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="32c63-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="32c63-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="32c63-121">-TypeName</span></span>
<span data-ttu-id="32c63-122">Nome do tipo de conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="32c63-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="32c63-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32c63-123">CommonParameters</span></span>
<span data-ttu-id="32c63-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32c63-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32c63-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32c63-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32c63-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32c63-126">INPUTS</span></span>

### <span data-ttu-id="32c63-127">System.String</span><span class="sxs-lookup"><span data-stu-id="32c63-127">System.String</span></span>

## <span data-ttu-id="32c63-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="32c63-128">OUTPUTS</span></span>

### <span data-ttu-id="32c63-129">System.String[]</span><span class="sxs-lookup"><span data-stu-id="32c63-129">System.String[]</span></span>

### <span data-ttu-id="32c63-130">System.String</span><span class="sxs-lookup"><span data-stu-id="32c63-130">System.String</span></span>

## <span data-ttu-id="32c63-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="32c63-131">NOTES</span></span>

## <span data-ttu-id="32c63-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32c63-132">RELATED LINKS</span></span>
