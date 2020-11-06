---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432735"
---
# <span data-ttu-id="34ebd-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="34ebd-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="34ebd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34ebd-102">SYNOPSIS</span></span>
<span data-ttu-id="34ebd-103">Exclui um contato de segurança.</span><span class="sxs-lookup"><span data-stu-id="34ebd-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34ebd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34ebd-104">SYNTAX</span></span>

### <span data-ttu-id="34ebd-105">SubscriptionLevelResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="34ebd-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ebd-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="34ebd-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ebd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="34ebd-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34ebd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34ebd-108">DESCRIPTION</span></span>
<span data-ttu-id="34ebd-109">Exclui um contato de segurança.</span><span class="sxs-lookup"><span data-stu-id="34ebd-109">Deletes a security contact.</span></span>

## <span data-ttu-id="34ebd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34ebd-110">EXAMPLES</span></span>

### <span data-ttu-id="34ebd-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="34ebd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="34ebd-112">Exclui o contato de segurança "default1"</span><span class="sxs-lookup"><span data-stu-id="34ebd-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="34ebd-113">OS</span><span class="sxs-lookup"><span data-stu-id="34ebd-113">PARAMETERS</span></span>

### <span data-ttu-id="34ebd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ebd-114">-DefaultProfile</span></span>
<span data-ttu-id="34ebd-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34ebd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ebd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34ebd-116">-InputObject</span></span>
<span data-ttu-id="34ebd-117">Objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="34ebd-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34ebd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="34ebd-118">-Name</span></span>
<span data-ttu-id="34ebd-119">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="34ebd-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ebd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34ebd-120">-PassThru</span></span>
<span data-ttu-id="34ebd-121">Retorne se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="34ebd-121">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34ebd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34ebd-122">-ResourceId</span></span>
<span data-ttu-id="34ebd-123">ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="34ebd-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34ebd-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34ebd-124">-Confirm</span></span>
<span data-ttu-id="34ebd-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ebd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ebd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ebd-126">-WhatIf</span></span>
<span data-ttu-id="34ebd-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34ebd-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34ebd-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34ebd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ebd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ebd-129">CommonParameters</span></span>
<span data-ttu-id="34ebd-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ebd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ebd-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ebd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ebd-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34ebd-132">INPUTS</span></span>

### <span data-ttu-id="34ebd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="34ebd-133">System.String</span></span>
<span data-ttu-id="34ebd-134">Microsoft. Azure. Commands. Security. cmdlets. SecurityContacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="34ebd-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="34ebd-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34ebd-135">OUTPUTS</span></span>

### <span data-ttu-id="34ebd-136">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="34ebd-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="34ebd-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34ebd-137">NOTES</span></span>

## <span data-ttu-id="34ebd-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34ebd-138">RELATED LINKS</span></span>
