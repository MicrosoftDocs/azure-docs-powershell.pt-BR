---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603222"
---
# <span data-ttu-id="33d44-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33d44-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="33d44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33d44-102">SYNOPSIS</span></span>
<span data-ttu-id="33d44-103">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33d44-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33d44-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33d44-105">DESCRIPTION</span></span>
<span data-ttu-id="33d44-106">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="33d44-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="33d44-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33d44-107">EXAMPLES</span></span>

### <span data-ttu-id="33d44-108">Excluir entidade de serviço do AAD.</span><span class="sxs-lookup"><span data-stu-id="33d44-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="33d44-109">Exclui a entidade de serviço do Azure Active Directory fornecida.</span><span class="sxs-lookup"><span data-stu-id="33d44-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="33d44-110">OS</span><span class="sxs-lookup"><span data-stu-id="33d44-110">PARAMETERS</span></span>

### <span data-ttu-id="33d44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d44-111">-DefaultProfile</span></span>
<span data-ttu-id="33d44-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="33d44-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33d44-113">-Force</span><span class="sxs-lookup"><span data-stu-id="33d44-113">-Force</span></span>
<span data-ttu-id="33d44-114">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="33d44-114">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="33d44-115">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="33d44-115">-ObjectId</span></span>
<span data-ttu-id="33d44-116">A ID de objeto da entidade de serviço a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="33d44-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33d44-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33d44-117">-PassThru</span></span>
<span data-ttu-id="33d44-118">Se especificado, retorna a entidade de serviço excluída.</span><span class="sxs-lookup"><span data-stu-id="33d44-118">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="33d44-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33d44-119">-Confirm</span></span>
<span data-ttu-id="33d44-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33d44-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d44-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d44-121">-WhatIf</span></span>
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

### <span data-ttu-id="33d44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d44-122">CommonParameters</span></span>
<span data-ttu-id="33d44-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d44-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d44-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d44-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33d44-125">INPUTS</span></span>

### <span data-ttu-id="33d44-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="33d44-126">None</span></span>
<span data-ttu-id="33d44-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="33d44-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33d44-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33d44-128">OUTPUTS</span></span>

### <span data-ttu-id="33d44-129">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33d44-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="33d44-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33d44-130">NOTES</span></span>
<span data-ttu-id="33d44-131">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="33d44-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="33d44-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33d44-132">RELATED LINKS</span></span>

[<span data-ttu-id="33d44-133">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33d44-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33d44-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33d44-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33d44-135">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="33d44-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="33d44-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="33d44-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="33d44-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="33d44-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
