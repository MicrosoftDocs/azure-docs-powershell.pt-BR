---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac4f7814898bcbfcee75c4a31273dfbcb6be7335
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775924"
---
# <span data-ttu-id="2d2e0-101">Set-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2d2e0-101">Set-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="2d2e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d2e0-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2e0-103">Atualiza o compartilhamento de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d2e0-103">Updates the share for a device.</span></span>

## <span data-ttu-id="2d2e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2d2e0-104">SYNTAX</span></span>

### <span data-ttu-id="2d2e0-105">SmbParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2d2e0-105">SmbParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -UserAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d2e0-106">UpdateByResourceIdSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2e0-106">UpdateByResourceIdSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2e0-107">UpdateByResourceIdNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2e0-107">UpdateByResourceIdNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -ResourceId <String> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2e0-108">UpdateByInputObjectSmbParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2e0-108">UpdateByInputObjectSmbParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -UserAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2e0-109">UpdateByInputObjectNfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2e0-109">UpdateByInputObjectNfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare -InputObject <PSDataBoxEdgeShare> -ClientAccessRight <Hashtable[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d2e0-110">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d2e0-110">NfsParameterSet</span></span>
```
Set-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ClientAccessRight <Hashtable[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d2e0-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2d2e0-111">DESCRIPTION</span></span>
<span data-ttu-id="2d2e0-112">Este **set-AzDataBoxEdgeShare** substituirá os direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="2d2e0-112">This **Set-AzDataBoxEdgeShare** will replace the access rights</span></span>

## <span data-ttu-id="2d2e0-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d2e0-113">EXAMPLES</span></span>

### <span data-ttu-id="2d2e0-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d2e0-114">Example 1</span></span>
```powershell
PS C:\> $AccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -ClientAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-2    NFS        Cloud            PageBlob         resource-group-name   storage-account-name
## $ClientAccessRights = @(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})
## Possible values for AccessRight options are 'NoAccess', 'ReadOnly', 'ReadWrite'
```

### <span data-ttu-id="2d2e0-115">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2d2e0-115">Example 2</span></span>
```powershell
PS C:\> $AccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
PS C:\> Set-AzDataBoxEdgeShare -ResourceGroupName resource-group-name -UserAccessRight $AccessRights
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resource-group-name   storage-account-name
## $UserAccessRights = @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})
## Possible values for AccessRight are 'Change', 'Read', 'Custom'
```

## <span data-ttu-id="2d2e0-116">OS</span><span class="sxs-lookup"><span data-stu-id="2d2e0-116">PARAMETERS</span></span>

### <span data-ttu-id="2d2e0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d2e0-117">-AsJob</span></span>
<span data-ttu-id="2d2e0-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2d2e0-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d2e0-119">-ClientAccessRight</span><span class="sxs-lookup"><span data-stu-id="2d2e0-119">-ClientAccessRight</span></span>
<span data-ttu-id="2d2e0-120">Acesso de leitura/gravação para clientIds, por exemplo: @ (@ {"ClientId" = "192.168.10.10"; " AccessRight "=" NoAccess "}, @ {" ClientId "=" 192.168.10.11 ";" AccessRight "=" ReadOnly "})</span><span class="sxs-lookup"><span data-stu-id="2d2e0-120">Read/Write Access for clientIds, For ex:@(@{"ClientId"="192.168.10.10";"AccessRight"="NoAccess"}, @{"ClientId"="192.168.10.11";"AccessRight"="ReadOnly"})</span></span>

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

### <span data-ttu-id="2d2e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2e0-121">-DefaultProfile</span></span>
<span data-ttu-id="2d2e0-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d2e0-123">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2d2e0-123">-DeviceName</span></span>
<span data-ttu-id="2d2e0-124">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="2d2e0-124">Device Name</span></span>

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

### <span data-ttu-id="2d2e0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d2e0-125">-InputObject</span></span>
<span data-ttu-id="2d2e0-126">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="2d2e0-126">Input Object</span></span>

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

### <span data-ttu-id="2d2e0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d2e0-127">-Name</span></span>
<span data-ttu-id="2d2e0-128">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="2d2e0-128">Resource Name</span></span>

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

### <span data-ttu-id="2d2e0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2e0-129">-ResourceGroupName</span></span>
<span data-ttu-id="2d2e0-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2d2e0-130">Resource Group Name</span></span>

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

### <span data-ttu-id="2d2e0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d2e0-131">-ResourceId</span></span>
<span data-ttu-id="2d2e0-132">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="2d2e0-132">Azure ResourceId</span></span>

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

### <span data-ttu-id="2d2e0-133">-UserAccessRight</span><span class="sxs-lookup"><span data-stu-id="2d2e0-133">-UserAccessRight</span></span>
<span data-ttu-id="2d2e0-134">forneça acesso à direita juntamente com nomes de usuário existentes para acessar tipos de compartilhamento SMB, por exemplo: @ (@ {"nome_do_usuário" = "User-Name-1"; " AccessRight "=" ler "}, @ {" username "=" User-Name-2 ";" AccessRight "=" ler "}, @ {" username "=" User-Name-3 ";" AccessRight "=" personalizado "})</span><span class="sxs-lookup"><span data-stu-id="2d2e0-134">provide access right along with existing usernames to access SMB Share types, For ex: @(@{"Username"="user-name-1";"AccessRight"="Read"}, @{"Username"="user-name-2";"AccessRight"="Read"}, @{"Username"="user-name-3";"AccessRight"="Custom"})</span></span>

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

### <span data-ttu-id="2d2e0-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2d2e0-135">-Confirm</span></span>
<span data-ttu-id="2d2e0-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d2e0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2e0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2e0-137">-WhatIf</span></span>
<span data-ttu-id="2d2e0-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d2e0-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d2e0-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d2e0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2e0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2e0-140">CommonParameters</span></span>
<span data-ttu-id="2d2e0-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2e0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2e0-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d2e0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2e0-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2d2e0-143">INPUTS</span></span>

### <span data-ttu-id="2d2e0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2d2e0-144">System.String</span></span>

### <span data-ttu-id="2d2e0-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2d2e0-145">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="2d2e0-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2d2e0-146">OUTPUTS</span></span>

### <span data-ttu-id="2d2e0-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2d2e0-147">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="2d2e0-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2d2e0-148">NOTES</span></span>

## <span data-ttu-id="2d2e0-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d2e0-149">RELATED LINKS</span></span>
