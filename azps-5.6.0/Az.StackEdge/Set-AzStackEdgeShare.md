---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: b127180b8eceea3c33ace0da86cfc700c1c7d113
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887289"
---
# <span data-ttu-id="0381e-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0381e-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="0381e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0381e-102">SYNOPSIS</span></span>
<span data-ttu-id="0381e-103">Atualiza o compartilhamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0381e-103">Updates the share for a device.</span></span>

## <span data-ttu-id="0381e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0381e-104">SYNTAX</span></span>

### <span data-ttu-id="0381e-105">SmbParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0381e-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0381e-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="0381e-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0381e-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0381e-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0381e-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="0381e-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0381e-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0381e-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0381e-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0381e-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0381e-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0381e-111">DESCRIPTION</span></span>
<span data-ttu-id="0381e-112">Este **Set-AzStackEdgeShare** substituirá os direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="0381e-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="0381e-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0381e-113">EXAMPLES</span></span>

### <span data-ttu-id="0381e-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0381e-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="0381e-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0381e-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="0381e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0381e-116">PARAMETERS</span></span>

### <span data-ttu-id="0381e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0381e-117">-AsJob</span></span>
<span data-ttu-id="0381e-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0381e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0381e-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="0381e-119">-ClientAccessRight</span></span>
<span data-ttu-id="0381e-120">Acesso de leitura/gravação para clientIds, para ex:@(@{"ClientId"="192.168.10.10";" AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";" AccessRight"="ReadOnly"})</span><span class="sxs-lookup"><span data-stu-id="0381e-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: UpdateByResourceIdNfsParameterSet, UpdateByInputObjectNfsParameterSet, NfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0381e-121">-DefaultProfile</span></span>
<span data-ttu-id="0381e-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0381e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0381e-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0381e-123">-DeviceName</span></span>
<span data-ttu-id="0381e-124">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="0381e-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0381e-125">-InputObject</span></span>
<span data-ttu-id="0381e-126">Objeto Input</span><span class="sxs-lookup"><span data-stu-id="0381e-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="0381e-127">-Name</span></span>
<span data-ttu-id="0381e-128">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="0381e-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0381e-129">-ResourceGroupName</span></span>
<span data-ttu-id="0381e-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0381e-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0381e-131">-ResourceId</span></span>
<span data-ttu-id="0381e-132">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="0381e-132">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdSmbParameterSet, UpdateByResourceIdNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="0381e-133">-UserAccessRight</span></span>
<span data-ttu-id="0381e-134">forneça acesso à direita juntamente com os nomes de usuário existentes para acessar tipos de Compartilhamento SMB, para ex: @(@{"Username"="user-name-1";" AccessRight"="Read"}, @{"Username"="user-name-2";" AccessRight"="Read"}, @{"Username"="user-name-3";" AccessRight"="Custom"})</span><span class="sxs-lookup"><span data-stu-id="0381e-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: SmbParameterSet, UpdateByResourceIdSmbParameterSet, UpdateByInputObjectSmbParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0381e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0381e-135">-Confirm</span></span>
<span data-ttu-id="0381e-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0381e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0381e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0381e-137">-WhatIf</span></span>
<span data-ttu-id="0381e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0381e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0381e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0381e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0381e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0381e-140">CommonParameters</span></span>
<span data-ttu-id="0381e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0381e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0381e-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0381e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0381e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0381e-143">INPUTS</span></span>

### <span data-ttu-id="0381e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="0381e-144">System.String</span></span>

### <span data-ttu-id="0381e-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0381e-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="0381e-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0381e-146">OUTPUTS</span></span>

### <span data-ttu-id="0381e-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0381e-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="0381e-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="0381e-148">NOTES</span></span>

## <span data-ttu-id="0381e-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0381e-149">RELATED LINKS</span></span>
