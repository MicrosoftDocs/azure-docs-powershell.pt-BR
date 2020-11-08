---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: 8bef754d7d9020193e4694953222a6579341c9ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112545"
---
# <span data-ttu-id="0a687-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0a687-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="0a687-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a687-102">SYNOPSIS</span></span>
<span data-ttu-id="0a687-103">Atualiza o compartilhamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a687-103">Updates the share for a device.</span></span>

## <span data-ttu-id="0a687-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a687-104">SYNTAX</span></span>

### <span data-ttu-id="0a687-105">SmbParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0a687-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a687-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a687-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a687-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a687-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a687-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a687-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a687-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a687-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a687-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a687-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a687-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a687-111">DESCRIPTION</span></span>
<span data-ttu-id="0a687-112">Este **set-AzDataBoxEdgeShare** substituirá os direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="0a687-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="0a687-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a687-113">EXAMPLES</span></span>

### <span data-ttu-id="0a687-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0a687-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="0a687-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0a687-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="0a687-116">OS</span><span class="sxs-lookup"><span data-stu-id="0a687-116">PARAMETERS</span></span>

### <span data-ttu-id="0a687-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a687-117">-AsJob</span></span>
<span data-ttu-id="0a687-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0a687-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a687-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="0a687-119">-ClientAccessRight</span></span>
<span data-ttu-id="0a687-120">Acesso de leitura/gravação para clientIds, por exemplo: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="0a687-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="0a687-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a687-121">-DefaultProfile</span></span>
<span data-ttu-id="0a687-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a687-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a687-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="0a687-123">-DeviceName</span></span>
<span data-ttu-id="0a687-124">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="0a687-124">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a687-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a687-125">-InputObject</span></span>
<span data-ttu-id="0a687-126">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="0a687-126">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: UpdateByInputObjectSmbParameterSet, UpdateByInputObjectNfsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a687-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a687-127">-Name</span></span>
<span data-ttu-id="0a687-128">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="0a687-128">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a687-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a687-129">-ResourceGroupName</span></span>
<span data-ttu-id="0a687-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0a687-130">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SmbParameterSet, NfsParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a687-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a687-131">-ResourceId</span></span>
<span data-ttu-id="0a687-132">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="0a687-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="0a687-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="0a687-133">-UserAccessRight</span></span>
<span data-ttu-id="0a687-134">forneça acesso à direita juntamente com nomes de usuário existentes para acessar tipos de compartilhamento SMB, por exemplo: @ (@ {"nome_do_usuário" = "User-Name-1"; " AccessRight "=" ler "}, @ {" username "=" User-Name-2 ";" AccessRight "=" ler "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizado "})</span><span class="sxs-lookup"><span data-stu-id="0a687-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="0a687-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a687-135">-Confirm</span></span>
<span data-ttu-id="0a687-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a687-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a687-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a687-137">-WhatIf</span></span>
<span data-ttu-id="0a687-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a687-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a687-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a687-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a687-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a687-140">CommonParameters</span></span>
<span data-ttu-id="0a687-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a687-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a687-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a687-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a687-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a687-143">INPUTS</span></span>

### <span data-ttu-id="0a687-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0a687-144">System.String</span></span>

### <span data-ttu-id="0a687-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0a687-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="0a687-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a687-146">OUTPUTS</span></span>

### <span data-ttu-id="0a687-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="0a687-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="0a687-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a687-148">NOTES</span></span>

## <span data-ttu-id="0a687-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a687-149">RELATED LINKS</span></span>
