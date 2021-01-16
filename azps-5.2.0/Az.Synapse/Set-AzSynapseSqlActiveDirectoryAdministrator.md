---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 4a2293384cdf2cf579458d05c112469d096bfd9a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261748"
---
# <span data-ttu-id="824a0-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="824a0-101">Set-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="824a0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="824a0-102">SYNOPSIS</span></span>
<span data-ttu-id="824a0-103">Provisiona um administrador do Azure AD para pool do SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="824a0-103">Provisions an Azure AD administrator for Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="824a0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="824a0-104">SYNTAX</span></span>

### <span data-ttu-id="824a0-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="824a0-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 -DisplayName <String> [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824a0-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="824a0-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> -DisplayName <String>
 [-ObjectId <Guid>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="824a0-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="824a0-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> -DisplayName <String> [-ObjectId <Guid>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824a0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="824a0-108">DESCRIPTION</span></span>
<span data-ttu-id="824a0-109">O cmdlet **set-AzSynapseSqlActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para o Azure Synapse espaço de trabalho de análise na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="824a0-109">The **Set-AzSynapseSqlActiveDirectoryAdministrator** cmdlet provisions an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace in the current subscription.</span></span>
<span data-ttu-id="824a0-110">Você pode provisionar apenas um administrador de cada vez.</span><span class="sxs-lookup"><span data-stu-id="824a0-110">You can provision only one administrator at a time.</span></span>
<span data-ttu-id="824a0-111">Os seguintes membros do Azure AD podem ser provisionados como administrador do espaço de trabalho de análise do Synapse:</span><span class="sxs-lookup"><span data-stu-id="824a0-111">The following members of Azure AD can be provisioned as a Synapse Analytics Workspace administrator:</span></span>
- <span data-ttu-id="824a0-112">Membros nativos do Azure AD</span><span class="sxs-lookup"><span data-stu-id="824a0-112">Native members of Azure AD</span></span> 
- <span data-ttu-id="824a0-113">Membros federados do Azure AD</span><span class="sxs-lookup"><span data-stu-id="824a0-113">Federated members of Azure AD</span></span> 
- <span data-ttu-id="824a0-114">Membros importados de outros anúncios do Azure que são membros nativos ou federados</span><span class="sxs-lookup"><span data-stu-id="824a0-114">Imported members from other Azure ADs who are native or federated members</span></span> 
- <span data-ttu-id="824a0-115">Grupos do Azure AD criados como grupos de segurança contas da Microsoft, como os dos domínios Outlook.com, Hotmail.com ou Live.com, não têm suporte como administradores.</span><span class="sxs-lookup"><span data-stu-id="824a0-115">Azure AD groups created as security groups Microsoft accounts, such as those in the Outlook.com, Hotmail.com, or Live.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="824a0-116">Não há suporte para outras contas de convidado, como aquelas dos domínios Gmail.com ou Yahoo.com como administradores.</span><span class="sxs-lookup"><span data-stu-id="824a0-116">Other guest accounts, such as those in the Gmail.com or Yahoo.com domains, are not supported as administrators.</span></span>
<span data-ttu-id="824a0-117">Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.</span><span class="sxs-lookup"><span data-stu-id="824a0-117">We recommend that you provision a dedicated Azure AD group as an administrator.</span></span>

## <span data-ttu-id="824a0-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="824a0-118">EXAMPLES</span></span>

### <span data-ttu-id="824a0-119">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="824a0-119">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs"
```

<span data-ttu-id="824a0-120">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="824a0-120">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="824a0-121">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="824a0-121">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
```

<span data-ttu-id="824a0-122">Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o espaço de trabalho chamado ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="824a0-122">This command provisions an Azure AD administrator group named DBAs for the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="824a0-123">Isso garante que o comando tenha êxito mesmo se o nome de exibição do grupo não for exclusivo.</span><span class="sxs-lookup"><span data-stu-id="824a0-123">This makes sure that the command succeeds even if the display name of the group is not unique.</span></span>

## <span data-ttu-id="824a0-124">OS</span><span class="sxs-lookup"><span data-stu-id="824a0-124">PARAMETERS</span></span>

### <span data-ttu-id="824a0-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="824a0-125">-AsJob</span></span>
<span data-ttu-id="824a0-126">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="824a0-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="824a0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824a0-127">-DefaultProfile</span></span>
<span data-ttu-id="824a0-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="824a0-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="824a0-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="824a0-129">-DisplayName</span></span>
<span data-ttu-id="824a0-130">Especifica o nome de exibição do usuário ou grupo para o qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="824a0-130">Specifies the display name of the user or group for whom to grant permissions.</span></span>
<span data-ttu-id="824a0-131">Este nome para exibição deve existir no Active Directory associado à assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="824a0-131">This display name must exist in the active directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="824a0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="824a0-132">-InputObject</span></span>
<span data-ttu-id="824a0-133">objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="824a0-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="824a0-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="824a0-134">-ObjectId</span></span>
<span data-ttu-id="824a0-135">Especifica a ID de objeto do usuário ou grupo no Azure Active Directory ao qual conceder permissões.</span><span class="sxs-lookup"><span data-stu-id="824a0-135">Specifies the object ID of the user or group in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="824a0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824a0-136">-ResourceGroupName</span></span>
<span data-ttu-id="824a0-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="824a0-137">Resource group name.</span></span>

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

### <span data-ttu-id="824a0-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="824a0-138">-ResourceId</span></span>
<span data-ttu-id="824a0-139">Identificador de recurso do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="824a0-139">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="824a0-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="824a0-140">-WorkspaceName</span></span>
<span data-ttu-id="824a0-141">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="824a0-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="824a0-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="824a0-142">-Confirm</span></span>
<span data-ttu-id="824a0-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824a0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824a0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824a0-144">-WhatIf</span></span>
<span data-ttu-id="824a0-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="824a0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824a0-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="824a0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824a0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824a0-147">CommonParameters</span></span>
<span data-ttu-id="824a0-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824a0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824a0-149">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="824a0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824a0-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="824a0-150">INPUTS</span></span>

### <span data-ttu-id="824a0-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="824a0-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="824a0-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="824a0-152">OUTPUTS</span></span>

### <span data-ttu-id="824a0-153">Microsoft. Azure. Commands. Synapse. Models. PSWorkspaceAadAdminInfo</span><span class="sxs-lookup"><span data-stu-id="824a0-153">Microsoft.Azure.Commands.Synapse.Models.PSWorkspaceAadAdminInfo</span></span>

## <span data-ttu-id="824a0-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="824a0-154">NOTES</span></span>

## <span data-ttu-id="824a0-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="824a0-155">RELATED LINKS</span></span>
