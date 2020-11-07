---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: EC6F7790-5E31-4C22-B006-38B5C1868671
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0272740ced33d19e2610a6116812df4a815ea3c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946188"
---
# <span data-ttu-id="4e143-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="4e143-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="4e143-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e143-102">SYNOPSIS</span></span>

## <span data-ttu-id="4e143-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e143-103">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-Enable] [[-CredentialName] <String>]
 [[-AzureKeyVaultUrl] <String>] [[-ServicePrincipalName] <String>] [[-ServicePrincipalSecret] <SecureString>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e143-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4e143-104">DESCRIPTION</span></span>

## <span data-ttu-id="4e143-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e143-105">EXAMPLES</span></span>

### <span data-ttu-id="4e143-106">1:</span><span class="sxs-lookup"><span data-stu-id="4e143-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="4e143-107">OS</span><span class="sxs-lookup"><span data-stu-id="4e143-107">PARAMETERS</span></span>

### <span data-ttu-id="4e143-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="4e143-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="4e143-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-110">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="4e143-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="4e143-111">-InformationAction</span></span>
<span data-ttu-id="4e143-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="4e143-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4e143-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4e143-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4e143-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="4e143-114">Continue</span></span>
- <span data-ttu-id="4e143-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="4e143-115">Ignore</span></span>
- <span data-ttu-id="4e143-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="4e143-116">Inquire</span></span>
- <span data-ttu-id="4e143-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4e143-117">SilentlyContinue</span></span>
- <span data-ttu-id="4e143-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="4e143-118">Stop</span></span>
- <span data-ttu-id="4e143-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="4e143-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4e143-120">-InformationVariable</span></span>
<span data-ttu-id="4e143-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="4e143-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="4e143-122">-Profile</span></span>
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

### <span data-ttu-id="4e143-123">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="4e143-123">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-124">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="4e143-124">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e143-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e143-125">CommonParameters</span></span>
<span data-ttu-id="4e143-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e143-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e143-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e143-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e143-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4e143-128">INPUTS</span></span>

## <span data-ttu-id="4e143-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4e143-129">OUTPUTS</span></span>

## <span data-ttu-id="4e143-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4e143-130">NOTES</span></span>

## <span data-ttu-id="4e143-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e143-131">RELATED LINKS</span></span>

