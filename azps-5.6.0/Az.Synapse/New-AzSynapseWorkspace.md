---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: 28f1486375e0efc1f9b1b3f9a18f12050dafd799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891919"
---
# <span data-ttu-id="35e55-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35e55-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="35e55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35e55-102">SYNOPSIS</span></span>
<span data-ttu-id="35e55-103">Cria um espaço de trabalho do Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="35e55-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="35e55-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="35e55-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35e55-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="35e55-105">DESCRIPTION</span></span>
<span data-ttu-id="35e55-106">O cmdlet **New-AzSynapseWorkspace** cria um espaço de trabalho do Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="35e55-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="35e55-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35e55-107">EXAMPLES</span></span>

### <span data-ttu-id="35e55-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35e55-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="35e55-109">Este comando cria um espaço de trabalho do Synapse Analytics chamado ContosoWorkspace que usa o Armazenamento de Dados ContosoAdlGenStorage, no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35e55-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="35e55-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="35e55-110">PARAMETERS</span></span>

### <span data-ttu-id="35e55-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35e55-111">-AsJob</span></span>
<span data-ttu-id="35e55-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="35e55-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35e55-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="35e55-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="35e55-114">O nome da conta de armazenamento padrão do ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="35e55-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="35e55-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="35e55-116">O sistema de arquivos padrão do ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="35e55-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35e55-117">-DefaultProfile</span></span>
<span data-ttu-id="35e55-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35e55-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35e55-119">-Location</span><span class="sxs-lookup"><span data-stu-id="35e55-119">-Location</span></span>
<span data-ttu-id="35e55-120">Região do Azure onde o recurso deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="35e55-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="35e55-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="35e55-122">Nome de uma rede virtual gerenciada pelo Synapse dedicada ao espaço de trabalho do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="35e55-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-123">-Name</span><span class="sxs-lookup"><span data-stu-id="35e55-123">-Name</span></span>
<span data-ttu-id="35e55-124">Nome do espaço de trabalho Synapse.</span><span class="sxs-lookup"><span data-stu-id="35e55-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35e55-125">-ResourceGroupName</span></span>
<span data-ttu-id="35e55-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="35e55-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="35e55-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="35e55-128">SQL credenciais de administrador.</span><span class="sxs-lookup"><span data-stu-id="35e55-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="35e55-129">-Tag</span></span>
<span data-ttu-id="35e55-130">Uma cadeia de caracteres, um dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="35e55-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35e55-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35e55-131">-Confirm</span></span>
<span data-ttu-id="35e55-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35e55-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35e55-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35e55-133">-WhatIf</span></span>
<span data-ttu-id="35e55-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35e55-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35e55-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35e55-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35e55-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35e55-136">CommonParameters</span></span>
<span data-ttu-id="35e55-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35e55-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35e55-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35e55-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35e55-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35e55-139">INPUTS</span></span>

### <span data-ttu-id="35e55-140">System.String</span><span class="sxs-lookup"><span data-stu-id="35e55-140">System.String</span></span>

### <span data-ttu-id="35e55-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="35e55-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="35e55-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="35e55-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="35e55-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="35e55-143">OUTPUTS</span></span>

### <span data-ttu-id="35e55-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="35e55-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="35e55-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="35e55-145">NOTES</span></span>

## <span data-ttu-id="35e55-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35e55-146">RELATED LINKS</span></span>
