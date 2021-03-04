---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 719ca5b8b837523359f4d55209956f7c68c3c93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890541"
---
# <span data-ttu-id="39836-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="39836-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="39836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39836-102">SYNOPSIS</span></span>
<span data-ttu-id="39836-103">Provisiona um administrador do Azure AD para o pool do Synapse Analytics SQL pool.</span><span class="sxs-lookup"><span data-stu-id="39836-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="39836-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="39836-104">SYNTAX</span></span>

### <span data-ttu-id="39836-105">SetByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="39836-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39836-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39836-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39836-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39836-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39836-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="39836-108">DESCRIPTION</span></span>
<span data-ttu-id="39836-109">O cmdlet **Set-AzSynapseSqlActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para o Espaço de Trabalho de Análise do Azure Synapse na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="39836-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="39836-110">Você pode provisioná-lo apenas um administrador por vez.</span><span class="sxs-lookup"><span data-stu-id="39836-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="39836-111">Os seguintes membros do Azure AD podem ser provisionados como administradores do Espaço de Trabalho do Synapse Analytics:</span><span class="sxs-lookup"><span data-stu-id="39836-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="39836-112">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="39836-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="39836-113">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="39836-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="39836-114">Membros importados de outros Azure ADs que são membros nativos ou federados</span><span class="sxs-lookup"><span data-stu-id="39836-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="39836-115">Grupos do Azure AD criados como grupos de segurança Contas da Microsoft, como aquelas nos domínios Outlook.com, Hotmail.com ou Live.com, não são suportadas como administradores.</span><span class="sxs-lookup"><span data-stu-id="39836-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="39836-116">Outras contas de convidado, como aquelas nos domínios Gmail.com Yahoo.com, não são suportadas como administradores.</span><span class="sxs-lookup"><span data-stu-id="39836-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="39836-117">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="39836-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="39836-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39836-118">EXAMPLES</span></span>

### <span data-ttu-id="39836-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39836-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="39836-120">Este comando provisiona um grupo de administradores do Azure AD chamado DBAs para o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="39836-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="39836-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="39836-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="39836-122">Este comando provisiona um grupo de administradores do Azure AD chamado DBAs para o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="39836-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="39836-123">Isso garante que o comando seja bem-sucedido, mesmo que o nome de exibição do grupo não seja exclusivo.</span><span class="sxs-lookup"><span data-stu-id="39836-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="39836-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="39836-124">PARAMETERS</span></span>

### <span data-ttu-id="39836-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39836-125">-AsJob</span></span>
<span data-ttu-id="39836-126">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="39836-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39836-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39836-127">-DefaultProfile</span></span>
<span data-ttu-id="39836-128">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39836-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39836-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="39836-129">-DisplayName</span></span>
<span data-ttu-id="39836-130">Especifica o nome de exibição do usuário ou grupo para quem conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="39836-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="39836-131">Esse nome de exibição deve existir no active directory associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="39836-131">This display name must exist in the active directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39836-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39836-132">-InputObject</span></span>
<span data-ttu-id="39836-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="39836-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39836-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="39836-134">-ObjectId</span></span>
<span data-ttu-id="39836-135">Especifica a ID do objeto do usuário ou grupo no Azure Active Directory para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="39836-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39836-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39836-136">-ResourceGroupName</span></span>
<span data-ttu-id="39836-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="39836-137">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39836-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39836-138">-ResourceId</span></span>
<span data-ttu-id="39836-139">Identificador de recursos do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="39836-139">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39836-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="39836-140">-WorkspaceName</span></span>
<span data-ttu-id="39836-141">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="39836-141">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39836-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39836-142">-Confirm</span></span>
<span data-ttu-id="39836-143">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39836-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39836-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39836-144">-WhatIf</span></span>
<span data-ttu-id="39836-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="39836-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39836-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39836-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39836-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39836-147">CommonParameters</span></span>
<span data-ttu-id="39836-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39836-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39836-149">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39836-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39836-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39836-150">INPUTS</span></span>

### <span data-ttu-id="39836-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="39836-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="39836-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="39836-152">OUTPUTS</span></span>

### <span data-ttu-id="39836-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="39836-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="39836-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="39836-154">NOTES</span></span>

## <span data-ttu-id="39836-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39836-155">RELATED LINKS</span></span>
