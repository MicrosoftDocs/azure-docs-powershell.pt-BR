---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 159CAD26-710A-4E65-B015-015A2C336A91
online version: ''
schema: 2.0.0
ms.openlocfilehash: a224ac58e6a8344953e29164de6ac6cfe0d00d97
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946000"
---
# <span data-ttu-id="38f5b-101">New-AzureProfile</span><span class="sxs-lookup"><span data-stu-id="38f5b-101">New-AzureProfile</span></span>

## <span data-ttu-id="38f5b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38f5b-102">SYNOPSIS</span></span>

## <span data-ttu-id="38f5b-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38f5b-103">SYNTAX</span></span>

### <span data-ttu-id="38f5b-104">Certificado</span><span class="sxs-lookup"><span data-stu-id="38f5b-104">Certificate</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Certificate <X509Certificate2> [<CommonParameters>]
```

### <span data-ttu-id="38f5b-105">ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="38f5b-105">ServicePrincipal</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> -Tenant <String> [-ServicePrincipal] [<CommonParameters>]
```

### <span data-ttu-id="38f5b-106">Permissão</span><span class="sxs-lookup"><span data-stu-id="38f5b-106">Token</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -AccessToken <String> -AccountId <String> [<CommonParameters>]
```

### <span data-ttu-id="38f5b-107">Credenciais</span><span class="sxs-lookup"><span data-stu-id="38f5b-107">Credentials</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] -SubscriptionId <String> [-StorageAccount <String>]
 -Credential <PSCredential> [-Tenant <String>] [<CommonParameters>]
```

### <span data-ttu-id="38f5b-108">Vazia</span><span class="sxs-lookup"><span data-stu-id="38f5b-108">Empty</span></span>
```
New-AzureProfile [-Environment <AzureEnvironment>] [<CommonParameters>]
```

### <span data-ttu-id="38f5b-109">Arquivos</span><span class="sxs-lookup"><span data-stu-id="38f5b-109">File</span></span>
```
New-AzureProfile -Path <String> [<CommonParameters>]
```

### <span data-ttu-id="38f5b-110">PropertyBag</span><span class="sxs-lookup"><span data-stu-id="38f5b-110">PropertyBag</span></span>
```
New-AzureProfile -Properties <Hashtable> [<CommonParameters>]
```

## <span data-ttu-id="38f5b-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38f5b-111">DESCRIPTION</span></span>

## <span data-ttu-id="38f5b-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38f5b-112">EXAMPLES</span></span>

### <span data-ttu-id="38f5b-113">1:</span><span class="sxs-lookup"><span data-stu-id="38f5b-113">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="38f5b-114">OS</span><span class="sxs-lookup"><span data-stu-id="38f5b-114">PARAMETERS</span></span>

### <span data-ttu-id="38f5b-115">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="38f5b-115">-AccessToken</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-116">-AccountId</span><span class="sxs-lookup"><span data-stu-id="38f5b-116">-AccountId</span></span>
```yaml
Type: String
Parameter Sets: Token
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-117">-Certificado</span><span class="sxs-lookup"><span data-stu-id="38f5b-117">-Certificate</span></span>
```yaml
Type: X509Certificate2
Parameter Sets: Certificate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-118">-Credential</span><span class="sxs-lookup"><span data-stu-id="38f5b-118">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-119">-Ambiente</span><span class="sxs-lookup"><span data-stu-id="38f5b-119">-Environment</span></span>
```yaml
Type: AzureEnvironment
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials, Empty
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-120">-Caminho</span><span class="sxs-lookup"><span data-stu-id="38f5b-120">-Path</span></span>
```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-121">-Propriedades</span><span class="sxs-lookup"><span data-stu-id="38f5b-121">-Properties</span></span>
```yaml
Type: Hashtable
Parameter Sets: PropertyBag
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-122">-UserPrincipal</span><span class="sxs-lookup"><span data-stu-id="38f5b-122">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="38f5b-123">-StorageAccount</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="38f5b-124">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: Certificate, ServicePrincipal, Token, Credentials
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-125">-Locatário</span><span class="sxs-lookup"><span data-stu-id="38f5b-125">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Credentials
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f5b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f5b-126">CommonParameters</span></span>
<span data-ttu-id="38f5b-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f5b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f5b-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f5b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f5b-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38f5b-129">INPUTS</span></span>

## <span data-ttu-id="38f5b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38f5b-130">OUTPUTS</span></span>

## <span data-ttu-id="38f5b-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38f5b-131">NOTES</span></span>

## <span data-ttu-id="38f5b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38f5b-132">RELATED LINKS</span></span>

