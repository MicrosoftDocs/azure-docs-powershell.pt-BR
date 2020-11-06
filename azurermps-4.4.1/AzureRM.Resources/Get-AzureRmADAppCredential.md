---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440966"
---
# <span data-ttu-id="40139-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="40139-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="40139-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="40139-102">SYNOPSIS</span></span>
<span data-ttu-id="40139-103">Recupera uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40139-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40139-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40139-104">SYNTAX</span></span>

### <span data-ttu-id="40139-105">ApplicationObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="40139-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40139-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40139-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40139-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="40139-107">DESCRIPTION</span></span>
<span data-ttu-id="40139-108">O cmdlet Get-AzureRmADAppCredential pode ser usado para recuperar uma lista de credenciais associadas a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40139-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="40139-109">Esse comando recuperará todas as propriedades de credenciais (mas não o valor da credencial) associado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40139-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="40139-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="40139-110">EXAMPLES</span></span>

### <span data-ttu-id="40139-111">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40139-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="40139-112">Retorna uma lista de credenciais associadas ao aplicativo com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="40139-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="40139-113">OS</span><span class="sxs-lookup"><span data-stu-id="40139-113">PARAMETERS</span></span>

### <span data-ttu-id="40139-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="40139-114">-ApplicationId</span></span>
<span data-ttu-id="40139-115">A ID do aplicativo do qual recuperar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="40139-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40139-116">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="40139-116">-ObjectId</span></span>
<span data-ttu-id="40139-117">A ID de objeto do aplicativo do qual as credenciais são recuperadas.</span><span class="sxs-lookup"><span data-stu-id="40139-117">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40139-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40139-118">-DefaultProfile</span></span>
<span data-ttu-id="40139-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="40139-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40139-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40139-120">CommonParameters</span></span>
<span data-ttu-id="40139-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40139-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40139-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40139-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40139-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="40139-123">INPUTS</span></span>

## <span data-ttu-id="40139-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="40139-124">OUTPUTS</span></span>

### <span data-ttu-id="40139-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="40139-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="40139-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="40139-126">NOTES</span></span>

## <span data-ttu-id="40139-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="40139-127">RELATED LINKS</span></span>

[<span data-ttu-id="40139-128">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="40139-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="40139-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="40139-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="40139-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="40139-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

