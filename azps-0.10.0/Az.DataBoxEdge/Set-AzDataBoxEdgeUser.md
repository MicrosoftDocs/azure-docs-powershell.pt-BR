---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: c344d5ac901e45c92c04a23cee252b1f747d4a83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775922"
---
# <span data-ttu-id="98f55-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="98f55-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="98f55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98f55-102">SYNOPSIS</span></span>
<span data-ttu-id="98f55-103">Define uma nova senha para um usuário no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98f55-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="98f55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f55-104">SYNTAX</span></span>

### <span data-ttu-id="98f55-105">SetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="98f55-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f55-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f55-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f55-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98f55-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f55-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98f55-108">DESCRIPTION</span></span>
<span data-ttu-id="98f55-109">O cmdlet **set-AzDataBoxEdgeUser** define uma nova senha para um usuário no dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="98f55-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="98f55-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98f55-110">EXAMPLES</span></span>

### <span data-ttu-id="98f55-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98f55-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="98f55-112">OS</span><span class="sxs-lookup"><span data-stu-id="98f55-112">PARAMETERS</span></span>

### <span data-ttu-id="98f55-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98f55-113">-AsJob</span></span>
<span data-ttu-id="98f55-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="98f55-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98f55-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f55-115">-DefaultProfile</span></span>
<span data-ttu-id="98f55-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98f55-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f55-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="98f55-117">-DeviceName</span></span>
<span data-ttu-id="98f55-118">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="98f55-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f55-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="98f55-119">-EncryptionKey</span></span>
<span data-ttu-id="98f55-120">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="98f55-120">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98f55-121">-InputObject</span></span>
<span data-ttu-id="98f55-122">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="98f55-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f55-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="98f55-123">-Name</span></span>
<span data-ttu-id="98f55-124">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="98f55-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f55-125">-Senha</span><span class="sxs-lookup"><span data-stu-id="98f55-125">-Password</span></span>
<span data-ttu-id="98f55-126">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="98f55-126">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f55-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f55-127">-ResourceGroupName</span></span>
<span data-ttu-id="98f55-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="98f55-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f55-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f55-129">-ResourceId</span></span>
<span data-ttu-id="98f55-130">ResourceId do Azure</span><span class="sxs-lookup"><span data-stu-id="98f55-130">Azure ResourceId</span></span>

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

### <span data-ttu-id="98f55-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="98f55-131">-Confirm</span></span>
<span data-ttu-id="98f55-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98f55-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f55-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f55-133">-WhatIf</span></span>
<span data-ttu-id="98f55-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98f55-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98f55-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98f55-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f55-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f55-136">CommonParameters</span></span>
<span data-ttu-id="98f55-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f55-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f55-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98f55-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f55-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98f55-139">INPUTS</span></span>

### <span data-ttu-id="98f55-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="98f55-140">None</span></span>

## <span data-ttu-id="98f55-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98f55-141">OUTPUTS</span></span>

### <span data-ttu-id="98f55-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="98f55-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="98f55-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98f55-143">NOTES</span></span>

## <span data-ttu-id="98f55-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98f55-144">RELATED LINKS</span></span>
