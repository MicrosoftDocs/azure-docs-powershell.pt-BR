---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946235"
---
# <span data-ttu-id="e853b-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e853b-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="e853b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e853b-102">SYNOPSIS</span></span>
<span data-ttu-id="e853b-103">Cria um objeto de configuração ACL vazio.</span><span class="sxs-lookup"><span data-stu-id="e853b-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="e853b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e853b-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e853b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e853b-105">DESCRIPTION</span></span>
<span data-ttu-id="e853b-106">O cmdlet **New-AzureAclConfig** cria um objeto de configuração do ACL (lista de controle de acesso) vazio.</span><span class="sxs-lookup"><span data-stu-id="e853b-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="e853b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e853b-107">EXAMPLES</span></span>

### <span data-ttu-id="e853b-108">Exemplo 1: criar um objeto de configuração de ACL</span><span class="sxs-lookup"><span data-stu-id="e853b-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="e853b-109">Esse comando cria um objeto de configuração ACL vazio e, em seguida, armazena-o na variável $Acl.</span><span class="sxs-lookup"><span data-stu-id="e853b-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="e853b-110">OS</span><span class="sxs-lookup"><span data-stu-id="e853b-110">PARAMETERS</span></span>

### <span data-ttu-id="e853b-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e853b-111">-InformationAction</span></span>
<span data-ttu-id="e853b-112">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e853b-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e853b-113">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e853b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e853b-114">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e853b-114">Continue</span></span>
- <span data-ttu-id="e853b-115">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e853b-115">Ignore</span></span>
- <span data-ttu-id="e853b-116">Inquire</span><span class="sxs-lookup"><span data-stu-id="e853b-116">Inquire</span></span>
- <span data-ttu-id="e853b-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e853b-117">SilentlyContinue</span></span>
- <span data-ttu-id="e853b-118">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e853b-118">Stop</span></span>
- <span data-ttu-id="e853b-119">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e853b-119">Suspend</span></span>

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

### <span data-ttu-id="e853b-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e853b-120">-InformationVariable</span></span>
<span data-ttu-id="e853b-121">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e853b-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e853b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e853b-122">CommonParameters</span></span>
<span data-ttu-id="e853b-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e853b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e853b-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e853b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e853b-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e853b-125">INPUTS</span></span>

## <span data-ttu-id="e853b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e853b-126">OUTPUTS</span></span>

## <span data-ttu-id="e853b-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e853b-127">NOTES</span></span>

## <span data-ttu-id="e853b-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e853b-128">RELATED LINKS</span></span>

[<span data-ttu-id="e853b-129">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e853b-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="e853b-130">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e853b-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="e853b-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="e853b-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


