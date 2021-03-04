---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 6abc37d37bf06025389329b8b917db8a75cefd1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890281"
---
# <span data-ttu-id="77211-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="77211-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="77211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77211-102">SYNOPSIS</span></span>
<span data-ttu-id="77211-103">Cria um novo usuário para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="77211-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="77211-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="77211-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77211-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="77211-105">DESCRIPTION</span></span>
<span data-ttu-id="77211-106">O cmdlet **New-AzDataBoxEdgeUser** cria um novo usuário para o dispositivo de Borda da Caixa de Dados.</span><span class="sxs-lookup"><span data-stu-id="77211-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="77211-107">Há suporte para a criação de apenas usuários `Share` do tipo.</span><span class="sxs-lookup"><span data-stu-id="77211-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="77211-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77211-108">EXAMPLES</span></span>

### <span data-ttu-id="77211-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77211-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="77211-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="77211-110">PARAMETERS</span></span>

### <span data-ttu-id="77211-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77211-111">-AsJob</span></span>
<span data-ttu-id="77211-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="77211-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77211-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77211-113">-DefaultProfile</span></span>
<span data-ttu-id="77211-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77211-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77211-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="77211-115">-DeviceName</span></span>
<span data-ttu-id="77211-116">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="77211-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77211-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="77211-117">-EncryptionKey</span></span>
<span data-ttu-id="77211-118">Chave de criptografia do dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="77211-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="77211-119">-Name</span><span class="sxs-lookup"><span data-stu-id="77211-119">-Name</span></span>
<span data-ttu-id="77211-120">Username</span><span class="sxs-lookup"><span data-stu-id="77211-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77211-121">-Password</span><span class="sxs-lookup"><span data-stu-id="77211-121">-Password</span></span>
<span data-ttu-id="77211-122">Senha, forneça como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="77211-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="77211-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77211-123">-ResourceGroupName</span></span>
<span data-ttu-id="77211-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="77211-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77211-125">-Type</span><span class="sxs-lookup"><span data-stu-id="77211-125">-Type</span></span>
<span data-ttu-id="77211-126">Selecionar UserType</span><span class="sxs-lookup"><span data-stu-id="77211-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77211-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77211-127">-Confirm</span></span>
<span data-ttu-id="77211-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77211-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77211-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77211-129">-WhatIf</span></span>
<span data-ttu-id="77211-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77211-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77211-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77211-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77211-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77211-132">CommonParameters</span></span>
<span data-ttu-id="77211-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77211-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77211-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77211-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77211-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77211-135">INPUTS</span></span>

### <span data-ttu-id="77211-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="77211-136">None</span></span>

## <span data-ttu-id="77211-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="77211-137">OUTPUTS</span></span>

### <span data-ttu-id="77211-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="77211-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="77211-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="77211-139">NOTES</span></span>

## <span data-ttu-id="77211-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77211-140">RELATED LINKS</span></span>
