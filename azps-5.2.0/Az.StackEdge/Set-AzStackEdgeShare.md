---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeShare.md
ms.openlocfilehash: 2b6c5d5f2295398975d912521ff6d0f001bbd3a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257012"
---
# <span data-ttu-id="3c0d4-101">Set-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3c0d4-101">Set-AzStackEdgeShare</span></span>

## <span data-ttu-id="3c0d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0d4-103">Atualiza o compartilhamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c0d4-103">Updates the share for a device.</span></span>

## <span data-ttu-id="3c0d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c0d4-104">SYNTAX</span></span>

### <span data-ttu-id="3c0d4-105">SmbParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c0d4-105">SmbParameterSet (Default)</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c0d4-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0d4-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0d4-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0d4-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0d4-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0d4-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0d4-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0d4-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzStackEdgeShare -InputObject <PSStackEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0d4-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0d4-110">NfsParameterSet</span></span>
```
Set-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c0d4-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c0d4-111">DESCRIPTION</span></span>
<span data-ttu-id="3c0d4-112">Este **set-AzStackEdgeShare** substituirá os direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="3c0d4-112">This **Set-AzStackEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="3c0d4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c0d4-113">EXAMPLES</span></span>

### <span data-ttu-id="3c0d4-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c0d4-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="3c0d4-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3c0d4-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzStackEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="3c0d4-116">OS</span><span class="sxs-lookup"><span data-stu-id="3c0d4-116">PARAMETERS</span></span>

### <span data-ttu-id="3c0d4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c0d4-117">-AsJob</span></span>
<span data-ttu-id="3c0d4-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3c0d4-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c0d4-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="3c0d4-119">-ClientAccessRight</span></span>
<span data-ttu-id="3c0d4-120">Acesso de leitura/gravação para clientIds, por exemplo: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="3c0d4-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="3c0d4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0d4-121">-DefaultProfile</span></span>
<span data-ttu-id="3c0d4-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0d4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0d4-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3c0d4-123">-DeviceName</span></span>
<span data-ttu-id="3c0d4-124">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="3c0d4-124">Device Name</span></span>

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

### <span data-ttu-id="3c0d4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c0d4-125">-InputObject</span></span>
<span data-ttu-id="3c0d4-126">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="3c0d4-126">Input Object</span></span>

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

### <span data-ttu-id="3c0d4-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c0d4-127">-Name</span></span>
<span data-ttu-id="3c0d4-128">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="3c0d4-128">Resource Name</span></span>

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

### <span data-ttu-id="3c0d4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0d4-129">-ResourceGroupName</span></span>
<span data-ttu-id="3c0d4-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3c0d4-130">Resource Group Name</span></span>

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

### <span data-ttu-id="3c0d4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c0d4-131">-ResourceId</span></span>
<span data-ttu-id="3c0d4-132">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="3c0d4-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="3c0d4-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="3c0d4-133">-UserAccessRight</span></span>
<span data-ttu-id="3c0d4-134">forneça acesso à direita juntamente com nomes de usuário existentes para acessar tipos de compartilhamento SMB, por exemplo: @ (@ {"nome_do_usuário" = "User-Name-1"; " AccessRight "=" ler "}, @ {" username "=" User-Name-2 ";" AccessRight "=" ler "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizado "})</span><span class="sxs-lookup"><span data-stu-id="3c0d4-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="3c0d4-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c0d4-135">-Confirm</span></span>
<span data-ttu-id="3c0d4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c0d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0d4-137">-WhatIf</span></span>
<span data-ttu-id="3c0d4-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c0d4-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c0d4-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c0d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0d4-140">CommonParameters</span></span>
<span data-ttu-id="3c0d4-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0d4-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c0d4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0d4-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c0d4-143">INPUTS</span></span>

### <span data-ttu-id="3c0d4-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3c0d4-144">System.String</span></span>

### <span data-ttu-id="3c0d4-145">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3c0d4-145">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3c0d4-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c0d4-146">OUTPUTS</span></span>

### <span data-ttu-id="3c0d4-147">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3c0d4-147">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3c0d4-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c0d4-148">NOTES</span></span>

## <span data-ttu-id="3c0d4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c0d4-149">RELATED LINKS</span></span>
