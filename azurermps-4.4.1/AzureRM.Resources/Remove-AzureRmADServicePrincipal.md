---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 0a2350cf3e1c8619e1860a6a5c4a0832c978d9de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609568"
---
# <span data-ttu-id="affed-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="affed-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="affed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="affed-102">SYNOPSIS</span></span>
<span data-ttu-id="affed-103">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="affed-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="affed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="affed-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="affed-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="affed-105">DESCRIPTION</span></span>
<span data-ttu-id="affed-106">Exclui a entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="affed-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="affed-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="affed-107">EXAMPLES</span></span>

### <span data-ttu-id="affed-108">--------------------------Excluir entidade de serviço AAD.</span><span class="sxs-lookup"><span data-stu-id="affed-108">--------------------------  Delete AAD service principal.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="affed-109">Exclui a entidade de serviço do Azure Active Directory fornecida.</span><span class="sxs-lookup"><span data-stu-id="affed-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="affed-110">OS</span><span class="sxs-lookup"><span data-stu-id="affed-110">PARAMETERS</span></span>

### <span data-ttu-id="affed-111">-Force</span><span class="sxs-lookup"><span data-stu-id="affed-111">-Force</span></span>
<span data-ttu-id="affed-112">{{Descrição da força de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="affed-112">{{Fill Force Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affed-113">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="affed-113">-ObjectId</span></span>
<span data-ttu-id="affed-114">A ID de objeto da entidade de serviço a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="affed-114">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="affed-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="affed-115">-PassThru</span></span>
<span data-ttu-id="affed-116">Se especificado, retorna a entidade de serviço excluída.</span><span class="sxs-lookup"><span data-stu-id="affed-116">If specified, returns the deleted service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affed-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="affed-117">-Confirm</span></span>
<span data-ttu-id="affed-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="affed-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affed-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="affed-119">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="affed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="affed-120">-DefaultProfile</span></span>
<span data-ttu-id="affed-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="affed-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="affed-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="affed-122">CommonParameters</span></span>
<span data-ttu-id="affed-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="affed-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="affed-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="affed-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="affed-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="affed-125">INPUTS</span></span>

## <span data-ttu-id="affed-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="affed-126">OUTPUTS</span></span>

### <span data-ttu-id="affed-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="affed-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="affed-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="affed-128">NOTES</span></span>
<span data-ttu-id="affed-129">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="affed-129">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="affed-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="affed-130">RELATED LINKS</span></span>

[<span data-ttu-id="affed-131">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="affed-131">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="affed-132">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="affed-132">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="affed-133">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="affed-133">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="affed-134">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="affed-134">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="affed-135">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="affed-135">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
