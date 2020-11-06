---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADGroup.md
ms.openlocfilehash: f9aa1f3d45a50a59c118abea4278bfed1725fa9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429371"
---
# <span data-ttu-id="d5842-101">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="d5842-101">Remove-AzureRmADGroup</span></span>

## <span data-ttu-id="d5842-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5842-102">SYNOPSIS</span></span>
<span data-ttu-id="d5842-103">Exclui um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5842-103">Deletes an active directory group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5842-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5842-104">SYNTAX</span></span>

### <span data-ttu-id="d5842-105">ObjectIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d5842-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADGroup -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5842-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5842-106">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroup -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5842-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5842-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmADGroup -InputObject <PSADGroup> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5842-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5842-108">DESCRIPTION</span></span>
<span data-ttu-id="d5842-109">Exclui um grupo do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5842-109">Deletes an active directory group.</span></span>

## <span data-ttu-id="d5842-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5842-110">EXAMPLES</span></span>

### <span data-ttu-id="d5842-111">Exemplo 1-remover um grupo por ID de objeto</span><span class="sxs-lookup"><span data-stu-id="d5842-111">Example 1 - Remove a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d5842-112">Remove o grupo com a ID de objeto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" do locatário.</span><span class="sxs-lookup"><span data-stu-id="d5842-112">Removes the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' from the tenant.</span></span>

### <span data-ttu-id="d5842-113">Exemplo 2-remover um grupo por tubulação</span><span class="sxs-lookup"><span data-stu-id="d5842-113">Example 2 - Remove a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroup
```

<span data-ttu-id="d5842-114">Obtém o grupo com a ID de objeto ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE ' e canaliza-se para Remove-AzureRmADGroup para remover o grupo do locatário.</span><span class="sxs-lookup"><span data-stu-id="d5842-114">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes that to Remove-AzureRmADGroup to remove the group from the tenant.</span></span>

## <span data-ttu-id="d5842-115">OS</span><span class="sxs-lookup"><span data-stu-id="d5842-115">PARAMETERS</span></span>

### <span data-ttu-id="d5842-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5842-116">-DefaultProfile</span></span>
<span data-ttu-id="d5842-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5842-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5842-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d5842-118">-DisplayName</span></span>
<span data-ttu-id="d5842-119">O nome de exibição do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d5842-119">The display name of the group to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5842-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d5842-120">-Force</span></span>
<span data-ttu-id="d5842-121">Se especificado, não pede confirmação para excluir o grupo.</span><span class="sxs-lookup"><span data-stu-id="d5842-121">If specified, doesn't ask for confirmation for deleting the group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5842-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5842-122">-InputObject</span></span>
<span data-ttu-id="d5842-123">A representação de objeto do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d5842-123">The object representation of the group to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5842-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d5842-124">-ObjectId</span></span>
<span data-ttu-id="d5842-125">A ID de objeto do grupo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d5842-125">The object id of the group to be removed.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5842-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5842-126">-PassThru</span></span>
<span data-ttu-id="d5842-127">Se o comando foi concluído, a especificação será retorna true se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d5842-127">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5842-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d5842-128">-Confirm</span></span>
<span data-ttu-id="d5842-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5842-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5842-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5842-130">-WhatIf</span></span>
<span data-ttu-id="d5842-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d5842-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5842-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5842-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5842-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5842-133">CommonParameters</span></span>
<span data-ttu-id="d5842-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5842-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5842-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5842-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5842-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5842-136">INPUTS</span></span>

### <span data-ttu-id="d5842-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d5842-137">System.Guid</span></span>

### <span data-ttu-id="d5842-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d5842-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="d5842-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d5842-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d5842-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5842-140">OUTPUTS</span></span>

### <span data-ttu-id="d5842-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5842-141">System.Boolean</span></span>

## <span data-ttu-id="d5842-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5842-142">NOTES</span></span>

## <span data-ttu-id="d5842-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5842-143">RELATED LINKS</span></span>
