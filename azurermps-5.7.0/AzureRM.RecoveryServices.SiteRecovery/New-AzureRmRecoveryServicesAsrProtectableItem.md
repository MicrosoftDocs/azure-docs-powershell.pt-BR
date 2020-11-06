---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrProtectableItem.md
ms.openlocfilehash: 8973c3606c7c29c254650b3412275c1dfd7bf761
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439834"
---
# <span data-ttu-id="0a00e-101">New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0a00e-101">New-AzureRmRecoveryServicesAsrProtectableItem</span></span>

## <span data-ttu-id="0a00e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a00e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a00e-103">Adicione (descubra) um servidor físico à lista de itens que protegem.</span><span class="sxs-lookup"><span data-stu-id="0a00e-103">Add(Discover) a physical server to the list of protectable items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a00e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a00e-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrProtectableItem -ProtectionContainer <ASRProtectionContainer>
 -FriendlyName <String> -IPAddress <String> -OSType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a00e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a00e-105">DESCRIPTION</span></span>
<span data-ttu-id="0a00e-106">O **New-AzureRmRecoveryServicesAsrProtectableItem** adiciona um novo item de proteção à lista de itens que protegem os itens que protegem em um contêiner de proteção em uma malha ASR (aplicável somente para o tipo de malha do VMware).</span><span class="sxs-lookup"><span data-stu-id="0a00e-106">The **New-AzureRmRecoveryServicesAsrProtectableItem** adds a new protectable item to the list of discovered protectable items in a protection container within an ASR fabric (applicable only for the VMware fabric type).</span></span>

## <span data-ttu-id="0a00e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a00e-107">EXAMPLES</span></span>

### <span data-ttu-id="0a00e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a00e-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrProtectableItem ProtectionContainer $pc -Name $name -IPAddress $ipaddresss -OSType $OsType
```

<span data-ttu-id="0a00e-109">Adicionar ou descobrir o novo serviço de recuperação do ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="0a00e-109">Add or Discover new Azure Recovery Service ProtectableItem.</span></span>

## <span data-ttu-id="0a00e-110">OS</span><span class="sxs-lookup"><span data-stu-id="0a00e-110">PARAMETERS</span></span>

### <span data-ttu-id="0a00e-111">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a00e-111">-Confirm</span></span>
<span data-ttu-id="0a00e-112">Solicite confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a00e-112">Prompt for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a00e-113">-DefaultProfile</span></span>
<span data-ttu-id="0a00e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a00e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0a00e-115">-FriendlyName</span></span>
<span data-ttu-id="0a00e-116">Nome amigável do item de proteção.</span><span class="sxs-lookup"><span data-stu-id="0a00e-116">Friendly name for the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="0a00e-117">-IPAddress</span></span>
<span data-ttu-id="0a00e-118">Endereço IP do item de proteção.</span><span class="sxs-lookup"><span data-stu-id="0a00e-118">IP address of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-119">-OSType</span><span class="sxs-lookup"><span data-stu-id="0a00e-119">-OSType</span></span>
<span data-ttu-id="0a00e-120">Tipo de sistema operacional (Windows/Linux) do item de proteção.</span><span class="sxs-lookup"><span data-stu-id="0a00e-120">Operating System type (Windows/Linux) of the protectable item.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a00e-121">-ProtectionContainer</span></span>
<span data-ttu-id="0a00e-122">Objeto de contêiner de proteção ASR ao qual o item que pode ser protegido deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="0a00e-122">ASR Protection container object to which the protectable item should be added.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a00e-123">-WhatIf</span></span>
<span data-ttu-id="0a00e-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a00e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a00e-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a00e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a00e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a00e-126">CommonParameters</span></span>
<span data-ttu-id="0a00e-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a00e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a00e-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a00e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a00e-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a00e-129">INPUTS</span></span>

### <span data-ttu-id="0a00e-130">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="0a00e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="0a00e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a00e-131">OUTPUTS</span></span>

### <span data-ttu-id="0a00e-132">Microsoft. Azure. Commands. Recoveryservices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a00e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a00e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a00e-133">NOTES</span></span>

## <span data-ttu-id="0a00e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a00e-134">RELATED LINKS</span></span>
